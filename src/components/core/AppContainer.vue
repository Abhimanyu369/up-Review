<template>
  <v-main>
    <app-bar></app-bar>
    <!-- <app-drawer /> -->
    <v-container>
      <v-fade-transition mode='out-in'>
        <router-view></router-view>
      </v-fade-transition>
    </v-container>
  </v-main>
</template>

<script>
import AppBar from '@/components/core/AppBar.vue';
// import AppDrawer from '@/components/core/AppDrawer.vue';

export default {
  name: 'AppContainer',
  components: {
    AppBar,
    // AppDrawer,
  },
};
</script>
