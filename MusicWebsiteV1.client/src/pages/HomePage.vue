<template>
  <div class="container-fluid">
    <div class="progress"></div>

    <div style="z-index: 0" class="cube-wrap parallax">
      <div style="z-index: 0" class="cube">
        <div style="z-index: 0" class="side top border"></div>
        <div style="z-index: 0" class="side bottom border"></div>
        <div style="z-index: 0" class="side front border"></div>
        <div style="z-index: 0" class="side back border"></div>
        <div style="z-index: 0" class="side left border"></div>
        <div style="z-index: 0" class="side right border"></div>
      </div>
    </div>
    <div style="z-index: 2" class="row mt-5">
      <div
        style="z-index: 2"
        class="col-4 rounded-bottom p-5 mt-5 text-primary mainfont bg-dark"
      >
        <h1 class="border-bottom tshadow">ABOUT</h1>
        <p class="text-white tshadow">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore,
          quasi. Accusamus perspiciatis eligendi et similique consequuntur! Rem,
          eius sint saepe voluptatem dolor delectus natus error aut blanditiis
          quis quae omnis quia aliquam harum similique quod distinctio
          asperiores. Tempora perspiciatis non dignissimos accusantium! Qui,
          animi facilis sed alias culpa necessitatibus reiciendis consectetur,
          eligendi facere accusamus accusantium cumque similique delectus libero
          natus? Impedit, dolorem, debitis facilis maiores aliquam ratione
          facere molestiae eos, nesciunt quisquam alias eligendi. Fugiat, quae
          dolore voluptatum, tempora error maiores, tenetur doloremque
          perferendis quasi quibusdam atque deserunt sit commodi molestias
          labore officiis similique dolorum? Eligendi qui fugiat quis nobis
          delectus commodi minima veniam, dolore iure, atque odio perferendis
          earum exercitationem dolorem voluptatem vel pariatur nihil doloribus
          unde.
        </p>
      </div>
      <div class="row justify-content-end">
        <div style="z-index: 2" class="col-7 mb-5 tshadow mainfont text-white">
          <h1>More</h1>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quasi
          impedit nostrum vel excepturi maxime deserunt eius suscipit
          exercitationem velit quam, esse cum debitis consequuntur aut nam
          dolorem neque fugit numquam totam qui. Fuga quos dolor vitae possimus
          officiis nostrum pariatur, aliquid laboriosam alias, molestias magni
          optio deleniti? Nisi culpa est doloremque incidunt, assumenda beatae
          maxime. Sed veritatis libero provident cumque esse officiis totam?
          Porro blanditiis molestias nesciunt a sapiente necessitatibus,
          officiis aut, quis incidunt in excepturi saepe, numquam quos quam.
          Neque, obcaecati ut. Cupiditate dolorem iure necessitatibus dolores
          eligendi ea quas nesciunt. Quos eos expedita doloremque placeat dicta
          similique reiciendis?
        </div>
      </div>
    </div>
  </div>
</template>


<script>

export default {

  name: 'Home',
}
window.addEventListener('scroll', () => {
  document.body.style.setProperty('--scroll', window.pageYOffset / (document.body.offsetHeight - window.innerHeight));
}, false);
</script>

<style scoped lang="scss">
.tshadow {
  text-shadow: rgba(0, 0, 0, 0.495) 1px 2px 6px;
}
.hoverable:hover {
  filter: drop-shadow(0px 0px 20px rgba(63, 255, 98, 0.603));
  transition: 444ms ease-in-out;
  cursor: pointer;
}
.parallax {
  // background-image: url("../assets/img/recurso-17MODERN_ICON.svg");
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
body {
  padding: 0;
  margin: 0;
  min-height: 500vh;
  background-color: rgb(139, 201, 228);
  animation: body 1s linear;
}
@keyframes body {
  to {
    background-color: rgb(19, 48, 97);
  }
}

.progress {
  height: 3px;
  width: 0%;
  background-color: #fff;
  position: fixed;
  top: 0;
  left: 0;
  animation: progress 1s linear;
}
@keyframes progress {
  to {
    background-color: rgb(20, 255, 226);
    width: 100%;
  }
}

.cube-wrap {
  --size: 35vmin;
  position: fixed;
  top: 55%;
  left: 66%;
  width: 0;
  height: 0;
  perspective: 100vmin;
}
.cube {
  transform-style: preserve-3d;
  transform: rotateX(0deg) rotateZ(45deg) rotateY(-45deg);
  animation: cube 10s linear;
}
@keyframes cube {
  to {
    transform: rotateX(360deg) rotateZ(45deg) rotateY(-45deg);
  }
}

.side {
  position: absolute;
  width: var(--size);
  height: var(--size);
  background-color: rgb(0, 0, 0);
  backface-visibility: visible;
  top: calc(var(--size) * -0.5);
  left: calc(var(--size) * -0.5);
}
.top {
  background-color: rgba(77, 255, 107, 0.444);
  transform: rotateX(90deg) translateZ(calc(var(--size) * 0.5));
}
.bottom {
  background-color: rgba(77, 255, 107, 0.444);
  transform: rotateX(90deg) translateZ(calc(var(--size) * -0.5));
}
.left {
  background-color: rgba(77, 255, 107, 0.444);
  transform: rotateY(90deg) translateZ(calc(var(--size) * 0.5));
}
.right {
  background-color: rgba(77, 255, 107, 0.444);
  transform: rotateY(90deg) translateZ(calc(var(--size) * -0.5));
}
.front {
  background-color: rgba(77, 255, 107, 0.444);
  transform: translateZ(calc(var(--size) * 0.5));
}
.back {
  background-color: rgba(77, 255, 107, 0.444);
  transform: translateZ(calc(var(--size) * -0.5));
}

:root * {
  /* Pause the animation */
  animation-play-state: paused;
  /* Bind the animation to scroll */
  animation-delay: calc(var(--scroll) * -1s);
  /* These last 2 properites clean up overshoot weirdness */
  animation-iteration-count: 1;
  animation-fill-mode: both;
}
</style>
