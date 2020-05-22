<template>
  <v-app id="inspire">
    <v-app-bar app dark absolute :flat="isFlat">
      <v-toolbar-title>
        <a href="#inspire">
          <v-icon class="welcomeIcon">fa-terminal</v-icon>Remco Goyvaerts
        </a>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn v-for="item in menu" :key="item.title" @click="scrollMeTo(item.link)" text>
          {{ item.title }}
          <v-icon class="navIcon" v-if="item.icon !== ''" right>{{ item.icon }}</v-icon>
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-content>
      <Header />
      <div ref="aboutMe">
        <AboutMe />
      </div>
      <div ref="projects">
        <Projects />
      </div>
      <Footer />
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import AboutMe from "./components/AboutMe";
import Projects from './components/Projects';
import Footer from './components/Footer';

export default {
  components: {
    Header,
    AboutMe,
    Projects,
    Footer
  },
  props: {
    source: String,
  },
  data () {
    return {
      menu: [{ icon: 'fa-address-card', title: 'About me', link: 'aboutMe' }, { icon: "fa-folder", title: "projects", link: 'projects' }],
      isFlat: true,
    };
  },
  methods: {
    scrollMeTo (refName) {
      var element = this.$refs[refName];
      var top = element.offsetTop;

      window.scrollTo(0, top);
    }
  }
};
</script>

<style lang="scss" scoped>
header {
  position: fixed !important;
}

.welcomeIcon {
  margin-right: 15px;
}

.navIcon {
  padding-left: 15px;
  padding-right: 15px;
}

a {
  text-decoration: none;
  color: white !important;
}
</style>
