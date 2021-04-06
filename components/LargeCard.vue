<template>
  <div class="col-md-4">
    <div class="card">
      <nuxt-link :to="'/products/'+card.id">
      <div class="card-img">
        <img :src="require('@/assets/images/'+card.image || card.image)" :alt="card.title" class="img-fluid">
      </div>
      </nuxt-link>
      <div class="card-title">
        <nuxt-link :to="'/products/'+card.id">{{card.title}}</nuxt-link>
      </div>
      <div class="card-text">
        {{card.snippet}}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LargeCard",
  props:['card']
}
</script>

<style scoped>

</style>
