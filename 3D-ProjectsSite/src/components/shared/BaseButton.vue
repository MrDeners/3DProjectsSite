<template lang="pug">
.wrapper
  h1 {{ label }}
</template>

<script setup lang="ts">
export interface Props {
  label: String
}

defineProps<Props>();
</script>

<style scoped lang="sass">

.wrapper
  height: 100%
  width: 100%
  text-align: center
  background-color: $light-paragraph-color

  h1
    color: $light-text-color
</style>
