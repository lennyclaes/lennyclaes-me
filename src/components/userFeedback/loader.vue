<template>
  <div class="loader"></div>
</template>

<script>
export default {
  name: "loader",
};
</script>

<style lang="scss" scoped>
.loader {
  width: 15px;
  height: 15px;
  background: black;
  border-radius: 90px;
  animation: loading 1s linear infinite alternate;
}

@keyframes loading {
  0% {
    transform: translateX(-40px);
    width: 15px;
  }
  50% {
    width: 80px;
  }
  100% {
    transform: translateX(40px);
    width: 15px;
  }
}
</style>