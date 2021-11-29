<template>
  <v-card>
    <template>
      <v-container class="grey lighten-5">
        <v-row>
          <v-col v-for="(n, i) in 12" :key="n" cols="12" md="4" xs="2">
            {{ i }}
            <div>
              <MyCard :cardid="i"></MyCard>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </template>
  </v-card>
</template>

<script>
import MyCard from '@/components/MyCard'

export default {
  name: 'Home',

  components: {
    MyCard
  }
}
</script>

<style scoped>
.line {
  display: flex;
}
</style>
