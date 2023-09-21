<template>
  <v-app dark>
    <div v-if="mobile > 1100">
      <Navbar />
      <v-app-bar elevation="0" dark>
        <v-btn
          icon
          @click.stop="rightDrawer = !rightDrawer"
          x-large
          v-if="mobile < 1100"
        >
          <v-icon x-large>mdi-menu</v-icon>
        </v-btn>
        <div class="btn-main" v-else>
          <v-btn text>
            <v-icon left>mdi-play-box</v-icon> Product & Services
          </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Promotions </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> News & Events </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Safety Tips </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> FAQS </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Location </v-btn>
        </div>
        <v-spacer></v-spacer>
        <v-icon class="facebook">mdi-facebook</v-icon>
        <v-icon class="twiter">mdi-twitter</v-icon>
        <v-icon class="youtube">mdi-youtube</v-icon>
      </v-app-bar>
    </div>
    <div v-else>
      <v-app-bar app elevation="0" dark fixed>
        <v-btn
          icon
          @click.stop="rightDrawer = !rightDrawer"
          x-large
          v-if="mobile < 1100"
        >
          <v-icon x-large>mdi-menu</v-icon>
        </v-btn>
        <div class="btn-main" v-else>
          <v-btn text>
            <v-icon left>mdi-play-box</v-icon> Product & Services
          </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Promotions </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> News & Events </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Safety Tips </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> FAQS </v-btn>
          <v-btn text> <v-icon left>mdi-play-box</v-icon> Location </v-btn>
        </div>
        <v-spacer></v-spacer>
        <v-icon class="facebook">mdi-facebook</v-icon>
        <v-icon class="twiter">mdi-twitter</v-icon>
        <v-icon class="youtube">mdi-youtube</v-icon>
        <v-icon v-if="mobile < 1100">mdi-magnify</v-icon>

      </v-app-bar>
      <NavbarMobile />
    </div>
    <v-main class="mb-10 pa-0">
      <Nuxt />
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app color="#ffffff" v-if="mobile > 1100">
      <v-row align="center" >
        <v-col cols="1" class="pr-0">
          <v-img :src="require('~/assets/images/SOne_index_logos.png')"> </v-img
        ></v-col>
        <v-col cols="11">
          <v-card elevation="0" dark class="pa-2">
            <span> Copyright &copy; 2014</span>
          </v-card>
        </v-col>
      </v-row>
    </v-footer>
    <v-footer :absolute="!fixed" app v-else dark>
      <span> Copyright &copy; 2014</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
      mobile: false,
    };
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  methods: {
    handleResize() {
      this.mobile = window.innerWidth;
    },
  },
};
</script>
<style lang="scss">
.facebook {
}

.facebook:hover {
  color: #286bd7;
}

.twiter:hover {
  color: #5ce4ff;
}

.youtube:hover {
  color: #ff1e1e;
}
</style>
