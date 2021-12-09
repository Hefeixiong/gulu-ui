<template>
  <article class="markdown-body" v-html="md">
  </article>
</template>

<script lang="ts">
import md from '../../markdown/intros.md';
export default {
  data() {
    return {md}
  }
}
</script>

<style lang="scss" scoped>

</style>
