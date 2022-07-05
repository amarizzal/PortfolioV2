<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      class="sidebar"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          class="sidebar__item"
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    
    <v-app-bar
      light
      color="white"
      elevate-on-scroll
      app
      class="navbar"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title></v-toolbar-title>

      <v-spacer></v-spacer>
      
      <v-btn 
        text 
        class="navbar__item text-capitalize mx-2 hidden-xs-only" 
        capitalize 
        nuxt
        to="/">
      About Me</v-btn>

      <v-btn 
        text 
        class="navbar__item text-capitalize mx-2 hidden-xs-only" 
        capitalize 
        to="/portfolio"
        nuxt>
      Portfolio</v-btn>

      <v-spacer></v-spacer>


      <!-- <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn> -->

<a href="https://drive.google.com/file/d/1jgB0Q3lpmKxWn4vexAvWY3jXsI_ed4Du/view?usp=sharing">
      <v-btn 
        depressed
        color="primary"
      >
        Download CV
      </v-btn>
      </a>
    </v-app-bar>
    <v-main >
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      app
      class="footer py-4"
      absolute
    >
      <v-row justify="center">
        <v-col>
          <v-row justify="center" class="p-4">
            <a class="footer__socialmedia" href="https://www.instagram.com/amarizzal_/" target="_blank" style="text-decoration: none" rel="noopener noreferrer">
              <v-btn
                icon
                class="mx-4 primary--text"
              >
                <v-icon size="24px">mdi-instagram</v-icon>
              </v-btn>
            </a>
            <a class="footer__socialmedia" href="https://www.linkedin.com/in/rizal-ammar-bb57b91b3/" target="_blank" style="text-decoration: none" rel="noopener noreferrer">
            <v-btn
              icon
              class="mx-4 primary--text"
            >
              <v-icon size="24px">mdi-linkedin</v-icon>
            </v-btn>
            </a>
          </v-row>
        </v-col>
        <v-col cols="12" class="footer__text text-center">
          <span>Build with love <span class="primary--text font-weight-bold"><3</span> by Rizal &copy; {{ new Date().getFullYear() }}</span>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/'
        },
        {
          icon: 'mdi-apps',
          title: 'Portfolio',
          to: '/portfolio'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@700&display=swap');

  a {
    text-decoration: none;
  }
</style>
