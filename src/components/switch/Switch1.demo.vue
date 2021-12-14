<demo>
常规用法
</demo>

<template>
  <Switch v-model:value="buttonStatus" />
</template>

<script lang="ts">
import Switch from '../../lib/Switch.vue'
import {
  ref
} from 'vue'
export default {
  components: {
    Switch,
  },
  setup() {
    const buttonStatus = ref(false)
    return {
      buttonStatus
    }
  }
}
</script>
