<template>
  <div class="filter"></div>
  <header>musicnote</header>
</template>

<script>
export default {
  name: "HeaderTitle",
};
</script>

<style scoped>
.filter {
  position: absolute;
  background-color: white;
  z-index: -10;
  height: 100vh;
  width: 100vw;
  -webkit-backdrop-filter: blur(2px);
  backdrop-filter: blur(2px) brightness(115%);
}

header {
  height: 105px;
  width: auto;
  line-height: 105px;
  text-align: center;
  font-size: 20px;
}
</style>
