<template>
  <div class="">
    <div class="container">
      <h6>All your item which you rented</h6>
      <div class="">
        <MyItem
          v-for="item in items"
          :key="item.id"
          :item="item"
        />
      </div>
    </div>
  </div>
</template>

<script>
import MyItem from "~/components/MyItem";
export default {
  name: "my-items",
  components: {MyItem},
  computed:{
    items(){
      return this.$store.getters.getRentalItem
    }
  }
}
</script>

<style scoped>

</style>
