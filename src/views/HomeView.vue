<template>
  <div class="home">
    <v-row justify="center">
      <v-img :src="underConstruction" max-width="700"></v-img>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Home",
  data: () => ({
    underConstruction: require("@/assets/img/underconstruction.jpg"),
  }),
  components: {},
};
</script>
