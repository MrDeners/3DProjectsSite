<template lang="pug">
BaseSectionName(:label='label')
v-container.section-wrapper(fluid)
  component(:is="widget", :cards = 'cards')


</template>

<script setup lang="ts">
import BaseSectionName from "../components/shared/BaseSectionName.vue";

defineProps({
  label: String,
  widget: Object
})

interface Card {
  title: string,
  image: string
}

const cards: Array<Card> = [];
cards.push({title: "Hello", image: ""});
cards.push({title: "World", image: ""});
cards.push({title: "Hello", image: ""});
cards.push({title: "World", image: ""});
cards.push({title: "Hello", image: ""});
cards.push({title: "World", image: ""});
cards.push({title: "Hello", image: ""});
cards.push({title: "World", image: ""});

</script>

<style scoped lang="sass">
.section-wrapper
  width: 95%
  background-color: $dark-wrapper-color
</style>
