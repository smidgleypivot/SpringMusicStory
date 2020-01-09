<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/SpringIcon.jpg"
          transition="scale-transition"
          width="40"
        />

<!--        <v-img-->
<!--          alt="Vuetify Name"-->
<!--          class="shrink mt-1 hidden-sm-and-down"-->
<!--          contain-->
<!--          min-width="100"-->
<!--          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"-->
<!--          width="100"-->
<!--        />-->
      </div>



      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>
    <v-spacer></v-spacer>

  <div class="container">
    <div class="d-flex">
  <div class="display-2">Spring Jukebox</div>
      <div> Please like all of your fav tunes</div>
    </div>
  </div>



    <SongVoter></SongVoter>
    <OfficeRadio></OfficeRadio>

    <v-content>

    </v-content>
  </v-app>
</template>

<script>
import SongVoter from './components/SongVoter';
import OfficeRadio from './components/OficeRadio';

export default {
  name: 'App',

  components: {
    OfficeRadio,
    SongVoter
  },

  data: () => ({}),
};
</script>
