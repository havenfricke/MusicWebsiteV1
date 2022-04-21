<template>
  <div class="container">
    <div id="#" class="row">
      <div>fhdjksahfdjklsahfjkdlshafjkdsa</div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
    </div>
    <div id="#about" class="row">
      <div>fhdjksahfdjklsahfjkdlshafjkdsa</div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
    </div>
    <div id="#portfolio" class="row">
      <div>fhdjksahfdjklsahfjkdlshafjkdsa</div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
    </div>
    <div id="#contact" class="row">
      <div>fhdjksahfdjklsahfjkdlshafjkdsa</div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
      <div class="p-5"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped lang="scss">
.home {
  display: grid;
  height: 80vh;
  place-content: center;
  text-align: center;
  user-select: none;
  .home-card {
    width: 50vw;
    > img {
      height: 200px;
      max-width: 200px;
      width: 100%;
      object-fit: contain;
      object-position: center;
    }
  }
}
</style>
