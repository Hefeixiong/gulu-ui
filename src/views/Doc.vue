<template>
  <div class="layout">
    <NavBar toggleMenuButtonVisible class="nav"/>
    <div class="content">
      <aside v-if="menuVisible">
        <h2>文档</h2>
        <ol>
          <li>
            <router-link to="/doc/intro">介绍</router-link>
          </li>
          <li>
            <router-link to="/doc/logs">更新日志</router-link>
          </li>
        </ol>
        <h2>组建列表</h2>
        <ol>
          <li>
            <router-link to="/doc/switch">Switch 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/button">Button 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/dialog">Dialog 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/tabs">Tabs 组件</router-link>
          </li>
        </ol>
        <h2>个人空间</h2>
        <ol>
          <li>
            <router-link to="/doc/blogs">博客</router-link>
          </li>
          <li>
            <a href="http://hefx.xyz/dist" target="_blank">旺财记账</a>
          </li>
        </ol>
      </aside>
      <main @click="toggleSide">
        <router-view/>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
import NavBar from '../components/NavBar.vue';
import {inject, Ref} from 'vue';

export default {
  components: {NavBar},
  setup() {
    const width = document.documentElement.clientWidth
    const menuVisible = inject<Ref<boolean>>('menuVisible'); // get
    const toggleSide = () => {
      if (width < 500) {
        menuVisible.value = false;
      }
    }
    return {
      menuVisible,
      toggleSide
    };
  },
};
</script>

<style lang="scss" scoped>
$aside-index: 10;
.layout {
  display: flex;
  flex-direction: column;
  height: 100vh;

  > .nav {
    flex-shrink: 0;
  }

  > .content {
    flex-grow: 1;
    padding-top: 60px;
    padding-left: 156px;
    @media (max-width: 500px) {
      padding-left: 0;
    }
  }
}

.content {
  display: flex;

  > aside {
    flex-shrink: 0;
  }

  > main {
    flex-grow: 1;
    padding-top: 16px;
    padding-left: 16px;
    padding-right: 16px;
    background: white;
  }
}

aside {
  background: white;
  width: 150px;
  position: fixed;
  padding: 86px 0 16px;
  top: 0;
  left: 0;
  height: 100%;
  z-index: $aside-index;
  box-shadow: 0 8px 8px #1296db;

  > h2 {
    margin-bottom: 4px;
    padding: 0 16px;
  }

  > ol {
    > li {
      > a {
        display: block;
        padding: 4px 16px;
        text-decoration: none;
      }

      .router-link-active {
        background: #cfcbcb;
      }
    }
  }
}

main {
  overflow: auto;
}
</style>
