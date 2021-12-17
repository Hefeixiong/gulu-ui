<template>
  <div>
    <h1>Button 示例</h1>
    <Demo :component="Common"/>
    <Demo :component="Disabled"/>
    <Demo :component="Level"/>
    <Demo :component="Size"/>
    <Demo :component="Loading"/>
  </div>
</template>

<script lang="ts">
import Common from './Button/Common.vue'
import Disabled from './Button/Disabled.vue'
import Level from './Button/Level.vue'
import Size from './Button/Size.vue'
import Loading from './Button/Loading.vue'
import Demo from './Demo.vue'
export default {
  components: {
    Demo
  },
  setup() {

    return {
      Common,
      Disabled,
      Level,
      Loading,
      Size
    };
  }
};
</script>

