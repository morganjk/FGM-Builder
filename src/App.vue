<template>
  <v-app class="black">
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar>

    <v-content>
     <Header/>
     <SaveModule/>
     
    </v-content>
  </v-app>
</template>

<script>
import Header from './components/Header';
import SaveModule from './components/SaveModule';

export default {
  name: 'App',
  components: {
    Header,
    SaveModule
  },
  data: () => ({
    
  }), 
};
</script>
