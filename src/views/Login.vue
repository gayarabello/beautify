<template>
  <div class="ma-8">
  <h1 class="mb-5"> Login </h1>
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
  </div>
</template>
