<template>
  <v-row color="white" justify="center" align="center">
    <v-col cols="12" sm="8" md="12">
      <v-row align="center"  class="my-16">
        <v-col cols="12" md="7" class="text-center text-md-left">
          <p class="font-weight-bold headline">Hello, I'm Rizal</p>
          <h1 class="display-3 primary--text my-2" style="font-weight: 700;" color="primary">Web Developer</h1>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugiat, ratione? Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque modi, amet asperiores sit provident optio.</p>
          <v-btn
            depressed
            color="primary"
            class="my-5"
            nuxt
            to="/portfolio"
          >
            My Portfolio
          </v-btn>
        </v-col>
        <v-col cols="12" md="5">
          <v-card style="height: 350px" flat class="grey lighten-2 rounded-lg"></v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
