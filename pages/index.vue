<template>
  <v-row color="white" justify="center" align="center">
    <v-col cols="12" sm="8" md="12">

      <!-- Jumbotron -->
      <v-row align="center"  class="my-16 pt-10">
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

      <!-- About Me -->
      <v-row align="center" class="my-16 py-16">
        <v-col cols="12" md="5" class="pt-10 pr-10">
          <v-card style="height: 200px" flat class="grey lighten-2 rounded-lg"></v-card>
        </v-col>
        <v-col cols="12" md="7" class="pt-10 text-center text-md-left">
          <h1 class="display-3 primary--text my-2 mb-13" style="font-weight: 700;" color="primary">About Me</h1>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Fugiat, ratione? Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque modi, amet asperiores sit provident optio.</p>
        </v-col>
      </v-row>

      <!-- Experience -->
      <v-row align="center"  class="my-16 pt-16">
        <v-col cols="12" class="">
          <h1 class="display-3 primary--text text-center my-2 mb-13 mx-auto" style="font-weight: 700;" color="primary">Experience</h1>
        </v-col>
        <v-col cols="12" class="">
          <v-timeline>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2019
                </span>
              </template>
              <div class="py-4">
                <h2 class="headline font-weight-light">
                  Lorem Ipsum
                </h2>
                <div class="">Lorem ipsum dolor sit amet consectetur adipisicing elit.</div>
              </div>
            </v-timeline-item>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2019
                </span>
              </template>
              <div class="py-4 text-right">
                <h2 class="headline font-weight-light">
                  Lorem Ipsum
                </h2>
                <div class="">Lorem ipsum dolor sit amet consectetur adipisicing elit.</div>
              </div>
            </v-timeline-item>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2019
                </span>
              </template>
              <div class="py-4">
                <h2 class="headline font-weight-light">
                  Lorem Ipsum
                </h2>
                <div class="">Lorem ipsum dolor sit amet consectetur adipisicing elit.</div>
              </div>
            </v-timeline-item>
          </v-timeline>
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
