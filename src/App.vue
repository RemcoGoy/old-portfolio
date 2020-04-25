<template>
  <v-app id="inspire">
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
        <v-btn v-for="item in menu" :key="item.title" :to="item.link" text>
          {{ item.title }}
          <v-icon right>{{ item.icon }}</v-icon>
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-content>
      <Header />
      <v-container fluid id="mainContent"></v-container>
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";

export default {
  components: {
    Header,
  },
  props: {
    source: String,
  },
  data() {
    return {
      menu: [{ icon: "fa-folder", title: "projects" }],
    };
  },
};
</script>
