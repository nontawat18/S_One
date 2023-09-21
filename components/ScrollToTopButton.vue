<template>
  <div>
    <v-btn
      @click="scrollToTop"
      class="scroll-to-top"
      elevation="0"
      fab
      color="transparent"
      v-if="showButton"
    >
      <v-img :src="require('~/assets/images/SOne_Mobile_top.png')"> </v-img>
    </v-btn>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showButton: false,
    };
  },

  mounted() {
    window.addEventListener("scroll", () => {
      if (window.scrollY == 0) {
        this.showButton = false;
      } else {
        this.showButton = true;
      }

    });
  },
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth", // Smooth scrolling animation
      });
    },
  },
};
</script>
<style scoped>
.scroll-to-top {
  position: fixed;
  bottom: 20px;
  right: 40%;
  background-color: transparent;
  color: #fff;
  border: none;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  text-align: center;
  cursor: pointer;
  z-index: 99;
}

.scroll-to-top {
  font-size: 24px;
  line-height: 40px;
}
</style>
