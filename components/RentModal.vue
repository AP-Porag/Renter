<template>
  <div>
    <b-button id="show-btn" @click="showModal" variant="outline-danger" block>Rent</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="calender-container d-flex">
        <div class="text-container px-1">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. At dignissimos doloremque doloribus hic, itaque nulla possimus quasi qui tempora voluptatum.</p>
        </div>
        <vc-date-picker
          class="px-1"
        :value="null"
        color="indigo"
        is-dark
        is-range
        />
      </div>
      <div class="container pt-2">
        <div class="row">
          <div class="col-md-6 col-sm-12">
            <b-button id="order" variant="outline-success" block>Order</b-button>
          </div>
          <div class="col-md-6 col-sm-12">
            <b-button class="mt-3" variant="outline-warning" @click="hideModal" block>Close Me</b-button>
          </div>
        </div>
      </div>
    </b-modal>
  </div>
</template>

<script>
export default {
  name:'Rent-Modal',
  methods: {
    showModal() {
      this.$refs['my-modal'].show()
    },
    hideModal() {
      this.$refs['my-modal'].hide()
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs['my-modal'].toggle('#toggle-btn')
    }
  }
}
</script>
