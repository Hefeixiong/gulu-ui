<template>
  <Switch :value="buttonStatus" @update:value="buttonStatus = $event"/>
</template>

<script lang="ts">
import Switch from '../lib/Switch.vue';
import {ref} from 'vue';

export default {
  components: {Switch},
  setup() {
    const buttonStatus = ref(false);
    return {buttonStatus};
  }
};
</script>

<style lang="scss" scoped>

</style>
