<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    item: {
      required: true
    }
  }
});
</script>

<template>
  <div>
    <div>change my text here for triggering HMR: HER</div>
    <div>{{ item }}</div>
  </div>
</template>