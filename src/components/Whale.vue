<template>
  <img
    class="whale"
    src="https://raw.githubusercontent.com/hsiuwennn/foresea0621/0886cd16b9bb7caedfc2de5d485c6bc102644083/img/whale.svg"
  />
</template>

<style lang="scss" scoped>
.whale {
  position: fixed;
  left: 40px;
  bottom: 50vh;
  width: 150px;
  height: 162px;
  animation-name: whale;
  animation-timing-function: ease-in-out;
  animation-direction: alternate;
  animation-duration: 2s;
  animation-iteration-count: infinite;
}

@keyframes whale {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(16px);
  }
}
</style>
