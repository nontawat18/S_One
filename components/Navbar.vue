<template>
  <div >
    <v-row class="pa-0" align="center">
      <v-col cols="3">
        <v-img :src="require('~/assets/images/SOne_index_logo.png')"> </v-img>
      </v-col>
      <v-col cols="5"></v-col>
      <v-col cols="4">
        <v-col>
          <v-row>
            <v-col cols="8"></v-col>
            <v-col cols="2">
              <v-hover v-slot="{ hover }">
                <v-card
                  :elevation="hover ? 0 : 0"
                  :class="{ 'on-hover': hover }"
                >
                  <v-img
                    :src="require('~/assets/images/SOne_index_iconthai.jpg')"
                  >
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
            <v-col cols="2">
              <v-hover v-slot="{ hover }">
                <v-card
                  :elevation="hover ? 0 : 0"
                  :class="{ 'on-hover': hover }"
                >
                  <v-img
                    :src="require('~/assets/images/SOne_index_iconeng.jpg')"
                  >
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>

        <v-col class="pt-0 pb-0">
          <v-text-field
            dense
            solo
            hide-details
            label="Search..."
            append-icon="mdi-magnify"
          ></v-text-field>
        </v-col>
        <v-col>
          <span style="border-right: solid 0.5px #000000; padding-right: 5px;">About S-ONE</span>
          <span style="border-right: solid 0.5px #000000; padding-right: 5px;">Job Opportunity</span>
          <span style="border-right: solid 0.5px #000000; padding-right: 5px;">Contact Us</span>
          <span>Site Map</span>
        </v-col>
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
.border{
  border-right: solid 0.5px #000000;
}
span {
  font-size: 14px;
}
span:hover {
  font-size: 14px;
  color: #f05a28;
}
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.4;
  background-color: rgba(0, 0, 0, 1) !important;
}
.background {
  background-color: rgba(0, 0, 0, 1) !important;
}
</style>
