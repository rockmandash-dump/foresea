<template>
  <div class="container">
    <KV />
    <Whale />
    <Ocean />
  </div>
</template>

<script>
import KV from "./components/KV";
import Whale from "./components/Whale";
import Ocean from "./components/Ocean";

export default {
  components: {
    KV,
    Whale,
    Ocean,
  },
};
</script>

<style lang="scss">
body {
  margin: 0;
  background-color: #0a233f;
  overflow-x: hidden;
  height: 3000px;
}

.container {
  position: relative;
  height: 100%;
}
</style>
