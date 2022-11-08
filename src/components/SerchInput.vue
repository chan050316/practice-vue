<template>
  <input
    class="searchSong"
    type="text"
    name="search"
    placeholder="Search song name"
  />
</template>

<script>
export default {
  name: "SerchInput",
};
</script>

<style scoped>
input {
  position: absolute;
  border-radius: 5px;
  width: 201px;
  height: 30px;
  right: 160px;
}
</style>
