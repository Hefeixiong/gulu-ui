<template>
  <Button loading>加载中</Button>
  <Button>加载完毕</Button>
</template>

<script lang="ts">
import Button from '../lib/Button.vue'
export default  {
  components: {Button},
  setup() {
    const onClick = () => {
      console.log('hi')
    }
    return {onClick}
  }
}
</script>

<style lang="scss" scoped>

</style>
