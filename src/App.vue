<template>
  <div id="app">
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

</style>
