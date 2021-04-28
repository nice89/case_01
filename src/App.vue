<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-btn
        class="mr-3"
        to="/"
      >
        home (case 1)
      </v-btn>

      <v-btn to="/about">
        about (case 2)
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>

<style lang="sass">
.box
  margin: 1rem
  padding: 1rem
  outline: 1px solid red
</style>