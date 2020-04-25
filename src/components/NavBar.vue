<template>
  <v-app-bar
    app
    dark
    flat
    absolute
    elevate-on-scroll
    scroll-target="#mainContent"
  >
    <v-toolbar-title>Portfolio</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn v-for="item in menu" :key="item.icon" :to="item.link" text>{{
        item.title
      }}</v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return { menu: [{ icon: "projects", title: "projects" }] };
  },
};
</script>

<style lang="scss" scoped></style>
