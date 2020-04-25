<template>
  <div class="aboutMe">
    <v-container>
      <v-row>
        <v-col :lg="8"></v-col>
        <v-col :lg="4">
          <v-img src="../assets/profile.jpg" aspect-ratio="1"></v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "AboutMe",
};
</script>

<style lang="scss" scoped>
.aboutMe {
  height: 60%;
  width: 100%;
  background: white;
  padding-top: 5%;
}
</style>
