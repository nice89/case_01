<template>
  <div class="box">
    <h1>Child {{ b }}</h1>

    <v-btn @click="$emit('callP')">
      child btn for call parent function
    </v-btn>

  </div>
</template>

<script>
export default {
  name: "HomeChild",

  props: {
    connect: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    b: 0
  }),

  methods: {
    logChild() {
      console.log(`I'm child method`)
    }
  },

  watch: {
    connect() {
      this.logChild()
      this.b++
    }
  }
}
</script>