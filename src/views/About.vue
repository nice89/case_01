<template>
  <div class="box">
    <h1>About {{ a }}</h1>

    <!--
    Simpler than Case 1.

    But, it is not suitable for use
    if you need to declare ref inside a loop.

    In loop case, you are interacting with the last child(ref)
    of the $refs array.
    -->

    <v-btn @click="$refs.child.logChild()">
      parent btn for call child function
    </v-btn>

    <about-child ref="child"/>

  </div>
</template>

<script>
import AboutChild from "../components/AboutChild.vue"

export default {
  name: 'Home',

  components: {
    AboutChild
  },

  data: () => ({
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