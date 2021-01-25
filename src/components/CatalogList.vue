<template>
  <div class="catalog_list mt-10">
    <v-tabs background-color="accent-3" height="140px">
      <v-tab v-for="i in 15" :key="i">
        <ul style="list-style: none; padding-left: 0px">
          <li>
            <img
              width="100px" alt=""
            />
          </li>
          <li>category {{ i }}</li>
        </ul>
      </v-tab>
    </v-tabs>
  </div>
</template>

<script>
export default {
  name: "CatalogList",
};
</script>

<style scoped>
</style>