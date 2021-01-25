<template>
  <div>
    <v-app-bar style="background-color: white" class=" align-center">
      <v-app-bar-nav-icon
        class="d-md-none"
        @click="drawer = true"
      ></v-app-bar-nav-icon>
      <v-toolbar-items class="d-none d-md-block"
        ><img src="../assets/logo.jpg" width="60" alt="mxfoodmart.com"
      /></v-toolbar-items>
      <v-toolbar-title class="mr-4  d-none d-md-block font-weight-bold">MX FOOD MART</v-toolbar-title>

      <!-- search bar -->

      <v-btn
        rounded
        class="justify-start search_box"
        width="260px"
        style="background-color: #eee"
        plain
      >
        <v-icon class="mr-1" color="grey">mdi-magnify</v-icon>
        <input
          type="text"
          v-on:keyup.enter="SearchProduct"
          v-model="search"
          placeholder=" Search products"
        />
      </v-btn>
      <!--  -->

      <v-spacer></v-spacer>

      <v-toolbar-items class="nav_link">
        <v-btn to="/" plain text class="black--text font-weight-bold">
          HOME
        </v-btn>

        <v-btn to="/about" text plain class="black--text font-weight-bold">
          ABOUT
        </v-btn>

        <v-btn to="/contact_us" text plain class="black--text font-weight-bold">
          CONTACT US
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),

  methods: {
    SearchProduct() {},
  },
};
</script>

<style scoped>
input:focus,
textarea:focus,
select:focus {
  outline: none;
}

@media (max-width: 650px) {
    .nav_link{
        display: none !important;
    }
}

@media (max-width: 650px) {
    .search_box{
        width: 90% !important;
    }
}


</style>