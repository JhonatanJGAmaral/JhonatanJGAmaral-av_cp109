<template>
  <v-app>
    <v-system-bar height="28" app>
      <h6>System bar</h6>
    </v-system-bar>

    <AppBar></AppBar>
    <Home></Home>

    <!-- <v-navigation-drawer>
      <div class="d-flex align-left"></div>
    </v-navigation-drawer> -->
    <v-navigation-drawer permanent left app>
      <v-list-item>
        <v-list-item-content>
          <br />
          <br />
          <template>
            <!-- <v-row justify="space-around"> -->
            <v-avatar>
              <img
                src="https://avatars.githubusercontent.com/u/70850413?s=400&u=8daad683b4b077c98723d25e8b266fd0aa3c741b&v=4"
                alt="John"
              />
            </v-avatar>
            <!-- </v-row> -->
          </template>
          <v-list-item-title class="text-h6">
            Trade President
          </v-list-item-title>
          <v-list-item-subtitle> About us </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <!-- card -->
      <v-card class="mx-auto" max-width="344">
        <v-card-text>
          <div>About our company</div>
          <p class="text-h4 text--primary">DO•IT•BY•YOURSELF</p>
          <!-- places•jobs•engagements•contribuitions -->
          <p>community</p>
          <div class="text--primary">
            Your home's here!<br />
            "a benevolent smilling place"
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="deep-purple accent-4"> Learn More </v-btn>
        </v-card-actions>
      </v-card>
      <!-- card -->
    </v-navigation-drawer>

    <!-- CAROUSEL -->
    <v-main> <router-view></router-view></v-main>
    <!-- FOOTER -->
    <v-footer dark padless app>
      <v-card flat tile class="indigo lighten-1 white--text text-center">
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0">
          Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet.
          Mauris cursus commodo interdum. Praesent ut risus eget metus luctus
          accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim
          a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula
          lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus
          iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum
          tempor vel ut orci. Orci varius natoque penatibus et magnis dis
          parturient montes, nascetur ridiculus mus.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer>
    <!-- --------------------------------------------- -->
  </v-app>
</template>

<script>
import AppBar from '@/components/AppBar'
import Home from '@/views/Home'

export default {
  name: 'App',
  components: {
    AppBar
  },
  views: {
    Home
  },
  data() {
    return {
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Photos', icon: 'mdi-image' },
        { title: 'About', icon: 'mdi-help-box' },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'
        }
      ],
      right: null,

      model: 0,
      colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange']
    }
  }
}
</script>
<style scoped>
.appbar {
  /* margin-top: 200px; */
}

h6 {
  color: rgb(132, 0, 255);
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
.margins {
  margin-bottom: 0;
}
</style>
