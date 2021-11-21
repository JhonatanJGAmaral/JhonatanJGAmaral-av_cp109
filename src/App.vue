<template>
  <v-app>
    <v-system-bar height="28" app>
      <h6>System bar</h6>
    </v-system-bar>

    <v-app-bar
      color="#6A76AB"
      dark
      absolute
      shrink-on-scroll
      prominent
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-3"
      permanent
      right
      class="appbar"
      app
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon src="">
        <!-- <a href=""></a> -->
      </v-app-bar-nav-icon>

      <v-app-bar-title>Dashboard</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab class="galery"> Galery</v-tab>
          <v-tab>Repositório</v-tab>
          <v-tab>Portfólio</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
    <!-- --------------------------------------------- -->
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
          <v-list-item-title class="text-h6"> Profile </v-list-item-title>
          <v-list-item-subtitle> career </v-list-item-subtitle>
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
          <div>About me</div>
          <p class="text-h4 text--primary">DO•IT•BY•YOURSELF</p>
          <!-- places•jobs•engagements•contribuitions -->
          <p>community</p>
          <div class="text--primary">
            well meaning and kindly.<br />
            "a benevolent smile"
          </div>
        </v-card-text>
        <v-card-actions>
          <v-btn text color="deep-purple accent-4"> Learn More </v-btn>
        </v-card-actions>
      </v-card>
      <!-- card -->
    </v-navigation-drawer>
    <!-- CAROUSEL -->
    <div class="tidyitup">
      <v-carousel v-model="model" class="ajusts" app>
        <v-carousel-item v-for="(color, i) in colors" :key="color">
          <v-sheet :color="color" height="100%" tile>
            <v-row class="fill-height" align="center" justify="center">
              <div class="text-h2">Slide {{ i + 1 }}</div>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>

      <template>
        <v-carousel class="ajusts-1" app>
          <v-carousel-item
            v-for="(item, i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
      </template>
    </div>
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
    <v-main>
      <!-- <router-view /> -->
    </v-main>
  </v-app>
</template>

<script>
export default {
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

.galery:hover .ajusts {
  display: none;
}

.galery:active.ajusts {
  display: none;
}
.ajusts {
  margin-top: 264px;
  margin-left: 264px;
  margin-right: auto;
  width: 800px;
  height: 1900px;
  display: inline;
}

.ajusts-1 {
  margin-top: 264px;
  margin-left: 10px;
  margin-right: auto;
  width: 1200px;
  height: 1900px;
  display: inline;
}

.tidyitup {
  display: flex;
}
</style>
