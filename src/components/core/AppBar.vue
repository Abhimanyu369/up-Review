<template>
  <div>
    <v-toolbar  style="background-color:transparent;color:#363472" dark>
      <v-toolbar-title>
         <strong style="font-family:Roboto; font-size:24px;">
            <v-icon large class="pa-2 pb-2"> mdi-star </v-icon>

            UpReview - Review Tracker</strong>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color='#363472' icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn color='#363472' icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn color='#363472' icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-toolbar>
    </div>
</template>
<script>
export default {
  name: 'AppBar',
  data () {
    return {
    };
  },
};
</script>
