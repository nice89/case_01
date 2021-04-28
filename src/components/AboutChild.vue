<template>
  <div class="box">
    <h1>Child {{ b }}</h1>

    <v-btn @click="$parent.logParent()">
      child btn for call parent function
    </v-btn>

  </div>
</template>

<script>
export default {
  name: "HomeChild",

  data: () => ({
    b: 0
  }),

  methods: {
    logChild() {
      console.log(`I'm child method`)
      this.b++
    }
  }
}
</script>