<template lang="pug">
.wrapper
  h1 {{ label }}

</template>

<script setup lang="ts">
import { defineProps } from 'vue'

defineProps({
  label: String,
  color: String
});
</script>

<style scoped lang="sass">
@import "../../../../3D-ProjectsSite/src/assets/styles/style.css"

.wrapper
  height: 100%
  width: 100%
  text-align: center
  padding: 2vh
  background-color: v-bind(color)

  h1
    @include text()
</style>
