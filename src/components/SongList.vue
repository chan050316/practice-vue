<template>
  <div class="section_Box">
    <div class="day_name">
      musiclist
      <div class="list_boxs">
        <div v-for="song of data" class="list" v-bind:key="song">
          <span class="material-icons deleteBtn">&#xe92e; </span>
          <span class="deleteSongName" style="display: none">{{
            song.name
          }}</span>
          <div class="list_Text">{{ song.name }} - {{ song.actor }}</div>
          <span class="material-icons copyBtn">&#xE14D;</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongList",
};
</script>

<style scoped>
section {
  height: 558px;
  width: auto;
  display: flex;
  justify-content: center;
}

section .section_Box {
  width: 500px;
  margin: 0 25px 0 25px;

  background-color: rgba(255, 255, 255, 0.3);
  -webkit-backdrop-filter: blur(5px);
  backdrop-filter: blur(5px);
  border-radius: 5px;
}

.section_Box .day_name {
  width: 230px;
  height: 40px;
  margin: 22px auto;
  border-radius: 5px;
  text-align: center;
  line-height: 40px;

  background-color: rgba(255, 255, 255, 0.3);
  -webkit-backdrop-filter: blur(30px);
  backdrop-filter: blur(30px) brightness(140%);
}

.section_Box .list_boxs {
  height: 474px;
  border-radius: 5px;

  background-color: rgba(255, 255, 255, 0.2);
  -webkit-backdrop-filter: blur(30px);
  backdrop-filter: blur(30px) brightness(125%);
  overflow: scroll;
}

.section_Box .list_boxs .list {
  height: 47px;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.section_Box .list_boxs .list .list_Text {
}

.section_Box .list_boxs .list .material-icons {
  margin-left: auto;
  margin-right: 5px;
  font-size: 15px;
  color: rgba(0, 0, 0, 0.7);
  cursor: pointer;
}

.section_Box .list_boxs .list .deleteBtn {
  margin-right: auto;
  margin-left: 7px;
}

.section_Box .list_boxs .list:hover {
  cursor: auto;
  transition-duration: 1s;
  background-color: rgba(255, 255, 255, 0.3);
  -webkit-backdrop-filter: blur(30px);
  backdrop-filter: blur(30px) brightness(125%);
}
</style>
