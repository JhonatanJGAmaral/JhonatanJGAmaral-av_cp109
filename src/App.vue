<template>
  <v-app>
    <template>
      <div>
        <v-system-bar window dark app>
          <v-icon>mdi-message</v-icon>
          <span>Go home</span>
          <v-spacer></v-spacer>
          <v-icon>mdi-minus</v-icon>
          <v-icon>mdi-checkbox-blank-outline</v-icon>
          <v-icon>mdi-close</v-icon>
        </v-system-bar>
      </div>
    </template>

    <AppBar> </AppBar>
    <Home></Home>

    <!-- <v-navigation-drawer>
      <div class="d-flex align-left"></div>
    </v-navigation-drawer> -->

    <!-- CAROUSEL -->
    <v-main> <router-view></router-view></v-main>

    <Footer></Footer>
    <AppDrawer></AppDrawer>
    <!-- --------------------------------------------- -->
  </v-app>
</template>

<script>
import AppBar from '@/components/AppBar'
import AppDrawer from '@/components/AppDrawer'
import Footer from '@/components/Footer'

export default {
  name: 'App',
  components: {
    AppBar,
    AppDrawer,
    Footer
  },

  data() {
    return {
      items: [
        { title: 'BUNGALLOWS', icon: 'mdi-view-dashboard' },
        { title: 'SEASIDE HOUSES', icon: 'mdi-image' },
        { title: 'CONDOMINIUM', icon: 'mdi-help-box' },
        { title: 'APARTMENT', icon: 'mdi-help-box' }
      ],
      right: null
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
