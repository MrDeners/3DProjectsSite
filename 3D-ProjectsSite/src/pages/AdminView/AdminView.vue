<template lang="pug">
header
  SectionName(label="Панель Администратора")  //TODO: Change text color
main
  BaseSection(label="Изображения на главной странице", :widget="BaseCatalogView")
</template>

<script setup lang="ts">
import BaseButton from "../../components/shared/BaseButton.vue";
import SectionName from "../../components/shared/BaseSectionName.vue";
import BaseCatalogView from "../../components/widgets/BaseCardsView.vue";
import BaseSection from "../../layouts/BaseSection.vue";

</script>

<style scoped lang="sass">

</style>
