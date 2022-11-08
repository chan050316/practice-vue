<template>
  <HeaderTitle />
  <SongList :items="songs" @delete-song="deleteSong" />
  <CreateForm :items="songs" @add-song="addSong" />
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
  methods: {
    addSong(song) {
      this.songs.push(song);
    },
    deleteSong(song) {
      console.log(song);
      this.songs = this.songs.filter(item => {
        return item !== song;
      });
    },
  },
  data() {
    return {
      songs: [
        {
          name: "aa",
          actor: "Aiaiai",
        },
        {
          name: "bb",
          actor: "Bibibib",
        },
      ],
    };
  },
};
</script>

<style>
@import "http://fonts.googleapis.com/icon?family=Material+Icons";
#app {
  background-image: url(./assets/img/morning.jpeg);
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
