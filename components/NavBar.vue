<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand class="text-decoration-none"><nuxt-link to="/">Renter</nuxt-link></b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item><nuxt-link to="/products">Products</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link to="/login">Login</nuxt-link></b-nav-item>
          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <b-dropdown-item><nuxt-link to="/profile">Profile</nuxt-link></b-dropdown-item>
            <b-dropdown-item><nuxt-link to="/my-items">My Items</nuxt-link></b-dropdown-item>
            <b-dropdown-item><nuxt-link to="/log-out">Log Out</nuxt-link></b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
name: "NavBar"
}
</script>

<style scoped>

</style>
