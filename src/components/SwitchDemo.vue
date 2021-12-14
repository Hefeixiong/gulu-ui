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

import 'prismjs'
import 'prismjs/themes/prism.css'

const Prism = (window as any).Prism

import {ref} from 'vue';

export default {
  components: {
    Demo
  },
  setup() {
    const buttonStatus = ref(false);
    return {
      buttonStatus,
      Switch1,
      Switch2,
      Prism
    };
  }
};
</script>

