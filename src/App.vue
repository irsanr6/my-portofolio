<template>
  <v-app>
    <v-nav class="text-center my-5">
      <router-link to="/">Home</router-link> | 
      <router-link to="/about">About</router-link>
    </v-nav>
    <v-main>
      <router-view />
    </v-main>
    <v-footer app color="light-blue lighten-3">
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} — <v-icon>mdi-instagram</v-icon
        ><strong
          ><a href="https://www.instagram.com/irsanramadhan13/" target="_blank"
            >irsanramadhan13</a
          ></strong
        >

        <span class="footer-content float-right"
          >v {{ version.slice(1, -1) }}</span
        >
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    version: JSON.stringify(require("@/../package.json").version),
  }),
};
</script>
