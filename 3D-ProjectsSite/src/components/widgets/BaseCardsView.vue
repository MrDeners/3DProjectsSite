<template lang="pug">
v-row
  v-col(v-for="card in cards" cols="6" sm="4" md="3" xl="2")
    BaseProjectCard(:isChanged='true' :title="card.title", :image="card.image")
  v-col(v-if="isChanged" cols="6" sm="4" md="3" xl="2")
    BaseProjectCard( :image="'https://habrastorage.org/r/w1560/getpro/habr/upload_files/106/d03/270/106d03270c016c1309719678f40dc4ad.png'")

</template>

<script setup lang="ts">

import BaseProjectCard from "../shared/BaseProjectCard.vue";

defineProps({
  cards: Array,
  isChanged: {type: Boolean, default: false}
})

</script>

<style scoped lang="sass">

</style>
