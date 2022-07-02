<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
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
    
    <!-- <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </v-app-bar> -->
    <v-app-bar
      light
      color="white"
      elevate-on-scroll
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title></v-toolbar-title>

      <v-spacer></v-spacer>
      
      <v-btn 
        text 
        class="text-capitalize mx-2 hidden-xs-only" 
        capitalize 
        nuxt
        to="/">
      About Me</v-btn>

      <v-btn 
        text 
        class="text-capitalize mx-2 hidden-xs-only" 
        capitalize 
        to="/portfolio"
        nuxt>
      Portfolio</v-btn>

      <v-btn 
        text 
        class="text-capitalize mx-2 hidden-xs-only" 
        capitalize 
        to="/contact"
        nuxt>
      Contact</v-btn>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-white-balance-sunny</v-icon>
      </v-btn>

      <!-- <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn> -->

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
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
      class="py-4"
      absolute
    >
      <v-row justify="center">
        <v-col>
          <v-row justify="center" class="p-4">
            <a href="https://www.instagram.com/amarizzal_/" target="_blank" style="text-decoration: none" rel="noopener noreferrer">
              <v-btn
                icon
                class="mx-4 primary--text"
              >
                <v-icon size="24px">mdi-instagram</v-icon>
              </v-btn>
            </a>
            <a href="https://www.linkedin.com/in/rizal-ammar-bb57b91b3/" target="_blank" style="text-decoration: none" rel="noopener noreferrer">
            <v-btn
              icon
              class="mx-4 primary--text"
            >
              <v-icon size="24px">mdi-linkedin</v-icon>
            </v-btn>
            </a>
          </v-row>
        </v-col>
        <v-col cols="12" class="text-center">
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
        {
          icon: 'mdi-chart-bubble',
          title: 'Contact',
          to: '/contact'
        }
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
</style>
