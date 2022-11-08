<template>
  <form class="createForm" action="/create" method="post">
    <input
      class="writeSong"
      type="text"
      name="name"
      placeholder="name"
      required
    />
    <input class="writeActor" type="text" name="actor" placeholder="actor" />
    <input type="submit" style="display: none" />
  </form>
</template>

<script>
export default {
  name: "CreateForm",
};
</script>

<style scoped>
form input {
  position: absolute;
  border-radius: 5px;
  width: 141px;
  height: 30px;
}

form .writeActor {
  left: 80px;
}

form .writeSong {
  left: 220px;
}
</style>
