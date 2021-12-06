<template>
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
        <v-list-item-title class="text-h6"> Trade President </v-list-item-title>
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
    <v-divider></v-divider>
    <v-card class="mx-auto format-1" max-width="344">
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
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'BUNGALLOWS', icon: 'mdi-view-dashboard' },
        { title: 'SEASIDE HOUSES', icon: 'mdi-image' },
        { title: 'CONDOMINIUM', icon: 'mdi-help-box' },
        { title: 'APARTMENT', icon: 'mdi-help-box' }
      ],
      right: null,

      model: 0,
      colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange']
    }
  }
}
</script>

<style scoped></style>
