<template>
  <div class="main-body">
    <LargeCardContainer
      v-for="largeCard in largeCards.slice(0,1)" :key="largeCard.id"
      :cardContainer="largeCard"
    />
    <SmallCardContainer
      v-for="smallCard in smallCards" :key="smallCard.id"
      :smallCardContainer="smallCard"
    />
  </div>
</template>

<script>
import {largeCardSections,smallCardSections} from "@/assets/data.js"
export default {
  data(){
    return{
      largeCards:largeCardSections,
      smallCards:smallCardSections,
    }
  }
}
</script>

<style>

</style>
