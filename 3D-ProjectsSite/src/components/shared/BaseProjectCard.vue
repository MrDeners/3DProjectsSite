<template lang="pug">
v-img.card.flex-column.align-end.justify-end(cover no-repeat center :src="image")
  v-img(v-if="isChanged" width="20" cover no-repeat center :src="close")
  .label(v-if="title != null")
    h1 {{ title }}

//v-img.card2(cover no-repeat center :src="image")
//  v-img.close(cover no-repeat center :src="close")
//  .label(v-if="title != null")
//    h1 {{ title }}

//.card2
//  img.close(src="https://cdn.icon-icons.com/icons2/1776/PNG/512/cross_114275.png")
//  .label(v-if="title != null")
//    h1 {{ title }}

</template>

<script setup lang="ts">

import {defineProps} from 'vue'

defineProps({
  title: { type: String, default: null },
  image: {type: String, default: 'https://guns.club/upload/resize_cache/medialibrary/2ef/o21s2k5he8wcy7ukq08b4by0t1xdpxdf/400_270_0/image1-kopiya.png'},
  isChanged: {type: Boolean, default: false}
})

const close: string = 'https://cdn.icon-icons.com/icons2/1776/PNG/512/cross_114275.png';
</script>

<style scoped lang="sass">

.card2
  width: 100%
  display: flex
  flex-direction: column
  justify-content: space-between

  aspect-ratio: 10/7
  border-radius: 20px
  background: url("https://guns.club/upload/resize_cache/medialibrary/2ef/o21s2k5he8wcy7ukq08b4by0t1xdpxdf/400_270_0/image1-kopiya.png")

.close
  width: 15%
  aspect-ratio: 1/1

.card
  aspect-ratio: 10/7
  border-radius: 20px

.label
  background: $white-wrapper-color
  text-align: center

  h1
    @include text($color: $dark-text-color, $size: 25px)  //TODO: Change to variables
</style>
