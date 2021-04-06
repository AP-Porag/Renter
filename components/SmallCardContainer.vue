<template>
  <div class="container">
    <h4>{{smallCardContainer.title}}</h4>
    <h6>{{smallCardContainer.snippet}}</h6>
    <div class="row card-container">
      <SmallCard
        v-for="card in smallCardContainer.cards" :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "SmallCardContainer",
  props:['smallCardContainer']
}
</script>

<style scoped>

</style>
