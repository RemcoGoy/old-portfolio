<template>
  <v-footer v-bind="localAttrs" :padless="true">
    <v-card flat tile width="100%" class="text-center">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon.icon" class="mx-4" icon>
          <a :href="icon.url" target="_blank">
            <v-icon>{{ icon.icon }}</v-icon>
          </a>
        </v-btn>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} —
        <strong>Remco Goyvaerts</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    icons: [
      { icon: 'fab fa-linkedin', url: 'https://www.linkedin.com/in/remco-goyvaerts-7878a945/' },
      { icon: 'fab fa-github', url: 'https://github.com/RemcoGoy' },
    ]
  })
}
</script>

<style lang="scss" scoped>
a {
  color: inherit !important;
  text-decoration: none;
}
</style>