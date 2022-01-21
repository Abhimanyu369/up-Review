<template>
  <div style="padding-bottom:20px">
    <v-row>
      <v-col v-for='n in 3'
      :key='n'
      class="">
    <v-card
      class='mx-auto .header-card'
      color='#ffffff'
      style="border-radius : 15px;"
      max-width='350'
      max-height='200'
    >
      <v-card-title>
        <v-icon large left> mdi-chart-bar </v-icon>
        <span class='text-h6 font-weight-light' style='font-family:Roboto'  >Review</span>
      </v-card-title>

      <v-card-text class='font-weight-bold' style='font-family:Roboto' >
        Easy and accurate
      </v-card-text>

      <v-card-actions>
        <v-list-item class='grow'>
          <v-list-item-avatar color='grey darken-3'>
            <v-img
              class='elevation-6'
              alt=''
              src='https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light'
            ></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>Paula G</v-list-item-title>
          </v-list-item-content>
            <v-icon class=''> mdi-star </v-icon>
            <span class='subheading'>5</span>
        </v-list-item>
      </v-card-actions>
    </v-card>
    </v-col>
    </v-row>
  </div>
</template>
<script>

