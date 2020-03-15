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
        href=""
        target="_blank"
        text
      >
        <span class="mr-2">Home</span>
      </v-btn>
      <v-btn
        href=""
        target="_blank"
        text
      >
        <span class="mr-2">Login</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-card width="400" class="mx-auto my-5">
        <v-card-title>
          Login
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field 
            label="Username">
            </v-text-field>
            <v-text-field
              :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show1 ? 'password' : 'text'"
              label="Password" 
              @click:append="show1 = !show1">
            </v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-btn text rounded href="" color="success"> Register </v-btn>
          <v-btn text rounded href="" color="info" depressed> Login </v-btn>


        </v-card-actions>
      </v-card>
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
        class="my-2"
      >
        {{ link }}
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
    </v-content>
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
        'Home',
        'Login',
      ],
  }),
};
</script>
