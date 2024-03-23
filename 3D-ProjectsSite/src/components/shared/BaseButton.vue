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
  margin: 3vh
  padding: 2vh
  border-radius: 20px

  h1
    @include text()   //TODO: Add root text size
</style>
