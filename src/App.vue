<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        :to="link.url"
        class="my-2"
      >
        {{ link.label }}
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view>
      </router-view>
    </v-content>
<v-footer
    color="primary lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        :to="link.url"
        class="my-2"
      >
        {{ link.label }}
      </v-btn>
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Beautify with Vuetify by Gaya Correia Dias Rabello </strong>
      </v-col>
    </v-row>
  </v-footer>
      <!-- <HelloWorld/> -->
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    //HelloWorld,
    
  },

  data: () => ({
    show1: false,
    links: [
        {
          label: 'Home',
          url: '/',
        },
        {
          label: 'Login',
          url: '/login',
        },
        {
          label: 'Dashboard',
          url: '/dashboard',
        }
      
      ],
  }),
};
</script>
