<template>
  <v-navigation-drawer app color="primary" permanent width="300">
    <v-list-item>
      <v-list-item-avatar>
        <v-img :src="myAvatar"></v-img>
      </v-list-item-avatar>
      <v-badge
        :value="hover"
        color="deep-purple accent-4"
        content="Hi Everyone, My Name Irsan"
        left
        offset-x="185"
        offset-y="40"
        transition="slide-x-transition"
      >
        <v-hover v-model="hover">
          <v-list-item-title>Irsan Ramadhan</v-list-item-title>
        </v-hover>
      </v-badge>
    </v-list-item>
    <v-divider></v-divider>
    <v-list nav>
      <v-list-item link v-for="menu in menus" :key="menu" :to="menu.link">
        <v-list-item-icon>
          <v-icon>{{ menu.icon }}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "Sidebar",
  data: () => ({
    myAvatar: require("@/assets/img/avatar.png"),
    hover: false,
    menus: [
      {
        title: "Dashboard",
        icon: "mdi-home",
        link: "/link1",
      },
      {
        title: "My Profile",
        icon: "mdi-account-box-multiple",
        link: "/link2",
      },
      {
        title: "WTF Project",
        icon: "mdi-projector",
        link: "/link3",
      },
      {
        title: "Contact",
        icon: "mdi-card-account-phone",
        link: "/link4",
      },
      {
        title: "About",
        icon: "mdi-information",
        link: "/link5",
      },
    ],
  }),
};
</script>

<style scoped>
</style>