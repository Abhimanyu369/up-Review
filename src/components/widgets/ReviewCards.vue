<template>
  <div style="padding-bottom: 20px">
    <v-row>
      <v-col v-for="n in 3" :key="n" class="">
        <v-card
          class="mx-auto card-class"
          color="#ffffff"
          style="border-radius: 15px"
          max-width="350"
          max-height="200"
          min-height="200"
        >
          <v-card-title v-if="n == 1">
            <v-icon large left> mdi-chart-bar </v-icon>
            <span class="text-h6 font-weight-light" style="font-family: Roboto ;color:#363472">
              Total Reviews</span
            >
          </v-card-title>
          <v-card-title v-if="n == 2">
            <v-icon large left> mdi-chart-bar </v-icon>
            <span class="text-h6 font-weight-light" style="font-family: Roboto"
              >Review Stats</span
            >
          </v-card-title>
          <v-card-title v-if="n == 3">
            <v-icon large left> mdi-chart-bar </v-icon>
            <span class="text-h6 font-weight-light" style="font-family: Roboto"
              >Review health</span
            >
          </v-card-title>

          <v-card-text
            class="font-weight-bold"
            style="font-family: Roboto; padding-left: 15%"
            v-if="n == 2"
          >
            <v-row
              v-for="(reviewitem, index) in reviewFilterData"
              :key="reviewitem[index]"
            >
              <v-rating
                readonly
                background-color="purple lighten-3"
                :value="index"
                color="#e75480"
                x-small
              >
              </v-rating>
              <b class="pr-2"> {{ reviewitem }}</b>
            </v-row>
          </v-card-text>

          <v-card-actions>
            <v-list-item class="grow">
              <v-list-item-avatar v-if="n == 1" color="grey darken-3">
                <v-img
                  class="elevation-6"
                  alt=""
                  src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                ></v-img>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title v-if="n == 1"
                  >Total Reviews</v-list-item-title
                >
                <!-- <v-list-item-title v-if="n == 2"
                  >Status</v-list-item-title
                > -->
                <v-list-item-title v-if="n == 3">
                  Current Status</v-list-item-title
                >
              </v-list-item-content>
              <!-- <v-icon class=""> mdi-star </v-icon> -->
              <span class="subheading" v-if="n == 1">
                <b> {{ reviewData && reviewData.length }}</b>
              </span>
              <span class="subheading" v-if="n == 2">
                <!-- <pre>{{ reviewFilterData }}</pre> -->
              </span>
              <span class="subheading" v-if="n == 3">
                <v-icon
                  large
                  color="#006400
"
                >
                  mdi-marker-check
                </v-icon>
                Good
              </span>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
import reviewData from "@/assets/reviewData.json";

export default {
  name: "ReviewCards",
  data() {
    return {
      reviewFilterData: [],
      reviewData: reviewData,
    };
  },
  beforeMount() {
    this.filtercardData();
  },
  methods: {
    filtercardData() {
      let overallUniqueValues = [];
      overallUniqueValues = reviewData.reduce((acc, val) => {
        acc[val.overall] =
          acc[val.overall] === undefined ? 1 : (acc[val.overall] += 1);
        return acc;
      }, {});
      console.log(overallUniqueValues);
      this.reviewFilterData = overallUniqueValues;
      this.getReviewHealthStats();
    },
    getReviewHealthStats() {
    },
  },
};
</script>
<style scoped>
.card-class {
  /* background: radial-gradient(#fcf5f6, transparent) !important; */
  color: #363472;
}
</style>

