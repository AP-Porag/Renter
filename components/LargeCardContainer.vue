<template>
<div class="container">
  <h4>{{cardContainer.title}}</h4>
  <h6>{{cardContainer.snippet}}</h6>
  <div class="row card-container">
    <LargeCard
      v-for="card in cardContainer.cards" :key="card.id"
      :card="card"
    />
  </div>
</div>
</template>

<script>
export default {
  name: "LargeCardContainer",
  props:['cardContainer']
}
</script>

<style scoped>

</style>
