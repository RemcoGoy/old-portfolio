<template>
  <div class="aboutMe">
    <v-container>
      <v-row>
        <v-col :lg="7">
          <div class="aboutHeader">About me</div>
          <v-list class="aboutList">
            <v-list-item class="aboutItem">
              <div class="aboutItemHead headline">General</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon color="black">fa-calendar-day</v-icon>
              <div class="aboutItemText">04/06/1999</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <div class="aboutItemHead headline">Achievements</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon color="black">fa-trophy</v-icon>
              <div class="aboutItemText">First place: Hack The Future</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon>fa-trophy</v-icon>
              <div
                class="aboutItemText subText"
              >A friend of mine and I were able to win the NLP Challenge at the Hack The Future Hackaton in October 2019.</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <div class="aboutItemHead headline">Education</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon color="black">fa-graduation-cap</v-icon>
              <div class="aboutItemText">IT Management</div>
            </v-list-item>
            <v-list-item class="aboutItem subItem">
              <v-icon>fa-graduation-cap</v-icon>
              <div class="aboutItemText subText">Immaculata instituut Oostmalle</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon>fa-graduation-cap</v-icon>
              <div class="aboutItemText subText">2011-2017</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon color="black">fa-graduation-cap</v-icon>
              <div class="aboutItemText">Applied Artificial Intelligence</div>
            </v-list-item>
            <v-list-item class="aboutItem subItem">
              <v-icon>fa-graduation-cap</v-icon>
              <div class="aboutItemText subText">Karel de Grote University College</div>
            </v-list-item>
            <v-list-item class="aboutItem">
              <v-icon>fa-graduation-cap</v-icon>
              <div class="aboutItemText subText">2017-2020</div>
            </v-list-item>
          </v-list>
        </v-col>
        <v-col :lg="1"></v-col>
        <v-col :lg="4">
          <v-img class="profileImage" src="../assets/profile.jpg" aspect-ratio="1"></v-img>
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
@import url("https://fonts.googleapis.com/css2?family=Comfortaa:wght@300;500;600&display=swap");

.aboutMe {
  height: 80vh;
  width: 100%;
  background: white;
  padding-top: 3%;
}

.aboutHeader {
  font-family: "Comfortaa", cursive;
  color: black;
  font-size: 4rem;
}

.profileImage {
  -webkit-box-shadow: 20px 20px 0px 0px #5fa4de;
  -moz-box-shadow: 20px 20px 0px 0px #5fa4de;
  box-shadow: 20px 20px 0px 0px #5fa4de;
}

.aboutList {
  background-color: white !important;
  color: black !important;
}

.aboutList > .aboutItem.theme--dark.v-list-item {
  color: black !important;
}

.aboutItemText {
  margin-left: 2%;
  font-family: "Comfortaa", cursive;
  font-weight: 600;
  font-size: 1rem;
}

.subText {
  font-size: 0.85rem;
  font-weight: 500;
  margin-top: -4%;
}

.subItem {
  margin-bottom: -4%;
}
</style>
