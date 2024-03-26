<template lang="pug">
.card
  .label(v-if="title != null" )
    h1 {{ title }}

</template>

<script setup lang="ts">

defineProps({
  title: { type: String, default: null },
  image: String
})
</script>

<style scoped lang="sass">
.card
  background: v-bind(image) no-repeat center
  background-size: cover
  border-radius: 20px

.label
  background: $white-wrapper-color
  display: flex
  justify-self: end
  text-align: center

  h1
    @include text($color: $dark-text-color, $size: 25px)  //TODO: Change to variables
</style>
