<template>
  <v-app id="inspire">
    <v-app-bar app dark absolute :flat="isFlat">
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
      <AboutMe />
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import AboutMe from "./components/AboutMe";

export default {
  components: {
    Header,
    AboutMe,
  },
  props: {
    source: String,
  },
  data() {
    return {
      menu: [{ icon: "fa-folder", title: "projects" }],
      isFlat: true,
    };
  },
};
</script>

<style lang="scss" scoped>
header {
  position: fixed !important;
}
</style>
