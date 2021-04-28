<template>
  <div class="box">
    <h1>Home {{ a }}</h1>

    <v-btn @click="tick = !tick">
      parent btn for call child function
    </v-btn>

    <home-child @callP="logParent" :connect="tick"/>

  </div>
</template>

<script>
import HomeChild from "../components/HomeChild"

export default {
  name: 'Home',

  components: {
    HomeChild
  },

  data: () => ({
    tick: false,
    a: 0
  }),

  methods: {
    logParent() {
      console.log(`I'm parent method`)
      this.a++
    }
  }
}
</script>
