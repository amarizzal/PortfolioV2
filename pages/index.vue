<template>
  <v-row color="white" justify="center" align="center">
    <v-col cols="12" sm="8" md="12">

      <!-- Jumbotron -->
      <v-row align="center" justify="center"  class="jumbotron my-3 my-lg-16 pt-10">
        <v-col cols="12" md="7" class="jumbotron__left text-center text-md-left px-10 px-md-0">
          <p class="font-weight-bold headline mb-10 mb-md-6 mb-lg-0">Hello, I'm Rizal</p>
          <h1 class="display-3 primary--text my-2 mb-10 mb-md-4" style="font-weight: 700;" color="primary">Web Developer</h1>
          <p>Menekuni bidang pengembangan website (web development) terutama pada pengembangan sisi depan yang bersinggungan langsung dengan user (Front-End).</p>
          <v-btn
            depressed
            color="primary"
            class="my-5 mt-10 mt-md-5 mt-lg-2"
            nuxt
            to="/portfolio"
          >
            My Portfolio
          </v-btn>
        </v-col>
        <v-col cols="12" class="jumbotron__right hidden-sm-and-down" md="5">
          <v-card style="height: 220px" flat class="grey lighten-2 rounded-lg">
            <v-img
              :src="require(`~/assets/img/jumbotron.jpg`)"
              contain class=""
            ></v-img>
          </v-card>
        </v-col>
      </v-row>

      <!-- About Me -->
      <v-row align="center" class="aboutme my-16 py-16">
        <v-col cols="12" md="5" class="aboutme__left hidden-sm-and-down pt-10 pr-10">
          <v-card style="height: 350px" flat class="grey lighten-2 rounded-lg mx-5">
            <v-img
              :src="require(`~/assets/img/aboutme.jpg`)"
              contain class=""
            ></v-img>
          </v-card>
        </v-col>
        <v-col cols="12" md="7" class="aboutme__right pt-10 text-center text-md-left">
          <h1 class="display-3 primary--text my-2 mb-13" style="font-weight: 700;" color="primary">About Me</h1>
          <p>Sedang menempuh pendidikan S1 Jurusan Teknik Informatika di UIN Maulana Malik Ibrahim Malang dan bertempat tinggal di Pesantren Mahasiswa Al-Hikam Malang.</p>
        </v-col>
      </v-row>

      <!-- Experience -->
      <v-row align="center"  class="experience my-16 pt-16">
        <v-col cols="12" class="experience__title">
          <h1 class="display-3 primary--text text-center my-2 mb-13 mx-auto" style="font-weight: 700;" color="primary">Experience</h1>
        </v-col>
        <v-col cols="12" class="experience__content">
          <v-timeline>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2022
                </span>
              </template>
              <div class="py-4">
                <h2 class="headline font-weight-bold">
                  Freelancer
                </h2>
                <div class="">Bekerja tim sebagai penanggung jawab tampilan website mulai desain hingga pengembangannya (UI/UX dan Front-End)</div>
              </div>
            </v-timeline-item>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2021
                </span>
              </template>
              <div class="py-4 text-right">
                <h2 class="headline font-weight-bold">
                  Front-End Web Developer
                </h2>
                <div class="">Bekerja di PT. Gumcode Indonesia mengembangkan tampilan web berdasarkan desain tim UI/UX serta mengintegrasikannya dengan Back-End.</div>
              </div>
            </v-timeline-item>
            <v-timeline-item>
              <template v-slot:opposite>
                <span class="font-weight-bold">
                  2019 - 2020
                </span>
              </template>
              <div class="py-4">
                <h2 class="headline font-weight-bold">
                  Magang
                </h2>
                <div class="">Bertugas slicing desain web ke project React dan Membuat tutorial framework css Tailwind</div>
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
