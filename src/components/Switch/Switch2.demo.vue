<demo>
支持 disabled
</demo>
<template>
  <Switch v-model:value="buttonStatus" disabled/>
</template>

<script lang="ts">
import Switch from '../../lib/Switch.vue';
import {ref} from 'vue';

export default {
  components: {
    Switch,
  },
  setup() {
    const buttonStatus = ref(false);
    return {
      buttonStatus
    };
  }
};
</script>
