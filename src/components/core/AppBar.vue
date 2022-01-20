<template>
  <div>
    <v-toolbar color='#26c6da' dark>
      <v-toolbar-title>
         <strong style="font-family:Roboto; font-size:24px;">
            <v-icon large class="pa-2 pb-2"> mdi-star </v-icon>

            UpReview - Review Tracker</strong>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
    </div>
</template>
<script>
export default {
  name: 'AppBar',
  data() {
    return {
    };
  },
};
</script>
