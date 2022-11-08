<template>
  <HeaderTitle />
  <SongList />
  <CreateForm />
  <SerchInput />
</template>

<script>
import HeaderTitle from "./components/HeaderTitle.vue";
import SongList from "./components/SongList.vue";
import CreateForm from "./components/CreateForm.vue";
import SerchInput from "./components/SerchInput.vue";

export default {
  name: "App",
  components: {
    HeaderTitle,
    SongList,
    CreateForm,
    SerchInput,
  },
};
</script>

<style>
#app {
  background-image: url(./assets/img/morning.jpeg);
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
