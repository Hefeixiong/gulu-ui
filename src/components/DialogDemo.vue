<template>
  <div>dialog 示例</div>
  <Demo :component="Dialog1" />
  <Demo :component="Dialog2" />
</template>

<script lang="ts">
import Demo from './Demo.vue'
import Dialog1 from './Dialog/Dialog1.demo.vue'
import Dialog2 from './Dialog/Dialog2.demo.vue'

export default {
  components: {
    Demo
  },
  setup() {
    return {
      Demo,
      Dialog1,
      Dialog2
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
