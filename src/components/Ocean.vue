<template>
  <div class="ocean">
    <div class="wave"></div>
    <div class="wave"></div>
    <OceanBottom />
  </div>
</template>

<script>
import OceanBottom from "./OceanBottom";

export default {
  components: {
    OceanBottom,
  },
};
</script>

<style lang="scss" scoped>
.ocean {
  width: 100%;
  height: 50vh;
  position: sticky;
  left: 0;
  top: 50vh;
  background: #015871;
  opacity: 0.6;
  margin: 50vh 0 0 0;
}

.wave {
  position: absolute;
  top: -198px;
  width: 6400px;
  height: 198px;

  background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg)
    repeat-x;
  animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite;
}

.wave:nth-of-type(2) {
  top: -175px;

  animation: wave 7s cubic-bezier(0.36, 0.45, 0.63, 0.53) -0.125s infinite,
    swell 7s ease -1.25s infinite;
}

@keyframes wave {
  0% {
    margin-left: 0;
  }
  100% {
    margin-left: -1600px;
  }
}

@keyframes swell {
  0%,
  100% {
    transform: translate3d(0, -25px, 0);
  }
  50% {
    transform: translate3d(0, 5px, 0);
  }
}
</style>
