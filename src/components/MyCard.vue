<template>
  <v-card class="mx-auto" max-width="400">
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://images.adsttc.com/media/images/533f/84a6/c07a/80d9/e300/00c1/large_jpg/seaside01.jpg?1396671625"
    >
      <v-card-title>Chose your home near to the beach</v-card-title>
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
