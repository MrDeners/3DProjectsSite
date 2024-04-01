<template lang="pug">
BaseSectionName(:label='label')
v-container.section-wrapper(fluid)
  component(:is='widget', :cards = 'cards', :isChanged='true')


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
cards.push({title: "Hello", image: "https://guns.club/upload/resize_cache/medialibrary/2ef/o21s2k5he8wcy7ukq08b4by0t1xdpxdf/400_270_0/image1-kopiya.png"});
cards.push({title: "Hello", image: "@/assets/images/text.png"});
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
