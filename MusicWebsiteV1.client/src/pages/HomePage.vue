<template>
  <div class="container-fluid parallax mt-5">
    <div class="mt-5"></div>
    <div class="mt-5"></div>
    <div class="mt-5 container row">
      <div class="mt-5 text-white">
        <div class="textfield1 col-6 mt-5 p-5">
          <div class="mt-5">
            <a class="mt-5 text-white">
              <span class="mt-5">
                <h1><a class="text-primary">TITLE</a></h1>
                <p class="mt-3 ms-5 p-5">
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Voluptates vel earum accusamus maxime ratione officia vitae
                  nulla quibusdam repudiandae deserunt blanditiis obcaecati
                  dignissimos ea veniam itaque eos aspernatur, odit eum incidunt
                  aliquid ut fugit provident voluptas. Excepturi, autem
                  repudiandae quas eveniet, expedita modi blanditiis optio iste
                  ad rem quidem dolorum! Accusamus sit dignissimos eos error
                  obcaecati placeat quasi deserunt facilis voluptas veritatis
                  dolorem numquam, rem doloremque et earum cumque? Quisquam
                  asperiores, quam saepe sed nobis consequuntur maxime, amet
                  repellendus iure natus quia earum culpa laborum sit molestias
                  facilis doloremque voluptatum iste veritatis soluta! Nulla
                  molestiae dignissimos delectus. Nam maxime numquam culpa fugit
                  ut qui, rerum cupiditate id accusamus omnis, dolor natus
                  blanditiis! Vero tempora possimus maxime, omnis nulla harum,
                  sit corporis facere provident necessitatibus iusto.
                </p>
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
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
.textfield1 {
  background-image: url("../assets/img/recurso-24CLIPPING_SHAPES.svg");
  background-size: cover;
  background-repeat: none;
  height: 100%;
  width: 100%;
}
</style>
