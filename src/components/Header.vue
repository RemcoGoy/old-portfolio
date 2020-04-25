<template>
  <div class="header">
    <v-container>
      <div class="helloText">hello<span class="dotSpan">.</span></div>
      <div class="mainText">
        I'm Remco Goyvaerts
      </div>
      <v-divider></v-divider>
      <div class="subText">
        A student <span class="dotSpan">Artificial Intelligence</span> from
        Belgium
      </div>

      <div class="btnGroup">
        <v-btn outlined color="blue lighten-2" class="contactBtn">
          <v-icon left color="blue lighten-2" class="ml-2 mr-4">
            fa-envelope
          </v-icon>
          Contact me
        </v-btn>
        <v-btn outlined color="blue lighten-2">
          <v-icon left color="blue lighten-2" class="ml-2 mr-4">
            fa-id-card
          </v-icon>
          My CV
        </v-btn>
      </div>
    </v-container>
  </div>
</template>

<script>
export default { name: "Header" };
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Comfortaa:wght@300;500;600&display=swap");

.helloText {
  font-family: "Comfortaa", cursive;
  font-size: 3.2rem;
  font-weight: 300;
}

.header {
  padding-top: 3%;
  height: 50%;
  width: 100%;
  background: #272727;
}

.dotSpan {
  color: #64b5f6;
}

.mainText {
  font-family: "Comfortaa", cursive;
  font-size: 4rem;
  font-weight: 600;
}

.subText {
  margin-top: 1%;
  font-family: "Comfortaa", cursive;
  font-size: 2rem;
  font-weight: 500;
}

.btnGroup {
  padding-top: 2%;
}

.contactBtn {
  margin-right: 1%;
}
</style>
