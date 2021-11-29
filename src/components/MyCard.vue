<template>
  <v-card class="mx-auto" max-width="400">
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://images.dwell.com/photos-6063391372700811264/6599016339180535808-large/on-a-hillside-in-los-angeles-architect-clive-wilkinson-created-a-three-story-home-for-himself-his-wife-elisabeth-and-their-children.jpg"
    >
      <v-card-title>Top 10 Boston Bungallows</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0"> Number 10 </v-card-subtitle>

    <v-card-text class="text--primary">
      <div>Whitehaven Beach</div>

      <div>Whitsunday Island, Whitsunday Islands</div>
    </v-card-text>

    <v-card-actions>
      <v-btn color="orange" text> {{ cardid }} </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({})
}
</script>
