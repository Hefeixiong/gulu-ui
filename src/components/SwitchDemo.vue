<template>
  <div>
    <h1>Switch组件示例</h1>
    <Demo :component="Switch1" />
    <Demo :component="Switch2" />
  </div>
</template>

<script lang="ts">
import Switch1 from './Switch/Switch1.demo.vue'
import Switch2 from './Switch/Switch2.demo.vue'
import Demo from './Demo.vue'


export default {
  components: {
    Demo
  },
  setup() {
    return {
      Switch1,
      Switch2
    };
  }
};
</script>

