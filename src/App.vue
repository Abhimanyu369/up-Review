<template>
  <div id="app">
    <!-- <v-img src='@/assets/hero-background.svg'></v-img> -->
    <app-container></app-container>
  </div>
</template>

<script>

import AppContainer from '@/components/core/AppContainer.vue';

export default {
  name: 'App',
  components: {
    AppContainer,
  },
};
</script>
<style lang="scss">
  @import "../node_modules/ag-grid-community/dist/styles/ag-grid.css";
  @import "../node_modules/ag-grid-community/dist/styles/ag-theme-material.css";
  @import url('https://fonts.googleapis.com/css2family=Roboto:wght@400;700&display=swap');
  $body-font-family: 'Roboto';
body {
 background-image: url("~@/assets/hero-background.svg");
 background-blend-mode: lighten;
}
::-webkit-scrollbar {
    width: 10px;
}
 
::-webkit-scrollbar-track {
    background-color: #ebebeb;
    -webkit-border-radius: 10px;
    border-radius: 10px;
}

::-webkit-scrollbar-thumb {
    -webkit-border-radius: 10px;
    border-radius: 10px;
/*     background: background: rgb(34,193,195); */
background: linear-gradient(257deg, rgba(34,193,195,1) 0%, rgba(215,147,237,1) 100%);; 
}
</style>
