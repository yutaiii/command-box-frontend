<template>
  <v-app>
    <v-app-bar
      app
      color="purple lighten-3"
      dark
    >
      <div class="logo-title">CommandBox</div>
      <v-spacer></v-spacer>

      <v-btn
        href="https://twitter.com/icchi_IT"
        target="_blank"
        text
      >
        <v-icon>mdi-twitter</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <CommandList/>
    </v-main>
  </v-app>
</template>

<script>
import CommandList from './components/CommandList';

export default {
  name: 'App',

  components: {
    CommandList,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
.logo-title {
  font-weight: bold;
  font-size: x-large;
  font-family: "Courier New", Courier, monospace;
}
</style>