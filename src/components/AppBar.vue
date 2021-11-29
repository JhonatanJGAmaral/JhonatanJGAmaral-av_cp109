<template>
  <v-app-bar
    color="#6A76AB"
    dark
    absolute
    shrink-on-scroll
    prominent
    src="https://images.adsttc.com/media/images/5b8d/e80e/f197/cc85/dc00/0113/original/GIF-01-.gif?1536026632"
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
        <v-tab class="galery"> Bungalows</v-tab>
        <v-tab>Seaside houses</v-tab>
        <v-tab>Condominium</v-tab>
        <v-tab>Apartment</v-tab>
      </v-tabs>
    </template>
  </v-app-bar>
</template>
