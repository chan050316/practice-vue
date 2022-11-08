<template>
  <form v-on:keyup.enter="addSong()">
    <input
      class="writeSong"
      type="text"
      name="name"
      placeholder="name"
      v-model="song.name"
    />
    <input
      class="writeActor"
      type="text"
      name="actor"
      placeholder="actor"
      v-model="song.actor"
    />
  </form>
</template>

<script>
export default {
  name: "CreateForm",
  data() {
    return {
      song: {},
    };
  },
  methods: {
    addSong() {
      this.$emit("add-song", this.song);
      this.song = {};
    },
  },
};
</script>

<style scoped>
input {
  position: absolute;
  border-radius: 5px;
  width: 141px;
  height: 30px;
}

.writeActor {
  left: 220px;
}

.writeSong {
  left: 80px;
}
</style>
