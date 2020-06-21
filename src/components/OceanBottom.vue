<template>
  <div class="OceanBottomContainer">
    <img src="../assets/story.png" />
  </div>
</template>

<script>
import { gsap, ScrollTrigger } from "gsap/all";

gsap.registerPlugin(ScrollTrigger);

export default {
  mounted() {
    gsap.to(".OceanBottomContainer > img", {
      x: "-100%",
      scrollTrigger: {
        trigger: ".OceanBottomContainer",
        start: "top center",
        end: "bottom top",
        scrub: true,
        markers: true,
      },
    });
  },
};
</script>

<style lang="scss" scoped>
.OceanBottomContainer {
  position: relative;
  width: 100%;
  height: 100%;

  > img {
    height: 100%;
  }
}
</style>
