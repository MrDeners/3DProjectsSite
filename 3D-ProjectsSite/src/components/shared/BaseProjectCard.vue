<template lang="pug">
.card3
  v-img.card-content(aspect-ratio="10/7" cover no-repeat center :src="image")
  v-img.close(v-if="isChanged" @click="deleteCard" cover no-repeat center :src="close")
  .label(v-if="title != null")
    .title {{ title }}
</template>

<script setup lang="ts">

import {defineProps} from 'vue'

const props = defineProps({
  id: { type: String, required: true },
  title: { type: String, default: null },
  image: {type: String, default: 'https://guns.club/upload/resize_cache/medialibrary/2ef/o21s2k5he8wcy7ukq08b4by0t1xdpxdf/400_270_0/image1-kopiya.png'},
  isChanged: {type: Boolean, default: false}
})

const close: string = 'https://cdn.icon-icons.com/icons2/1776/PNG/512/cross_114275.png';

const emit = defineEmits(['deleteCard'])

function deleteCard() {
  emit('deleteCard', props.id);
}
</script>

<style scoped lang="sass">

//.card-content
//  width: 100%
//  aspect-ratio: 10/7
//  position: absolute
//
//.card3
//  position: relative
//  width: 100%
//  aspect-ratio: 10/7
//  border-radius: 20px
//  display: flex
//  flex-direction: column
//  //align-items: flex-end
//
//.close
//  justify-self: start
//  align-self: end
//
//.gap
//  gap: 70%

.card-content
  width: 100%
  aspect-ratio: 10/7
  position: absolute
  border-radius: 20px

.card3
  position: relative
  width: 100%
  aspect-ratio: 10/7
  border-radius: 20px
  display: grid
  align-items: end

.close
  width: 10%
  justify-self: end
  align-self: start
  margin: 4%

.label
  background: var(--white-wrapper-color)
  text-align: center
  z-index: 1
  border-radius: 0 0 20px 20px

  .title
    @include text($color: $dark-text-color, $size: 25px)  //TODO: Change to variables
</style>
