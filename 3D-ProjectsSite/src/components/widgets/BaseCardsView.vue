<template lang="pug">
v-row()
  v-col.px-12(v-for="card in cards" cols="4")
    BaseProjectCard(:title="card.title", :image="card.image" )

</template>

<script setup lang="ts">

import BaseProjectCard from "../shared/BaseProjectCard.vue";

defineProps({
  cards: Array
})

</script>

<style scoped lang="sass">

</style>
