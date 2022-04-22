<template>
  <div class="container-fluid parallax mt-5"></div>
</template>


<script>

export default {
  name: 'Home'
}
</script>

<style scoped lang="scss">
.hoverable:hover {
  filter: drop-shadow(0px 0px 20px rgba(63, 255, 98, 0.603));
  transition: 444ms ease-in-out;
  cursor: pointer;
}
.parallax {
  background-image: url("../assets/img/recurso-17MODERN_ICON.svg");
  height: 100vh;
  width: 100%;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.mainfont {
  font-family: monospace;
}
</style>
