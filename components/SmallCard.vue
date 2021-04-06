<template>
  <div class="col-md-3">
    <nuxt-link :to="'/products/'+card.id">
    <div class="card">
        <img :src="require('@/assets/images/'+card.image)" alt="">
    </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "SmallCard",
  props:['card']
}
</script>

<style scoped>

</style>
