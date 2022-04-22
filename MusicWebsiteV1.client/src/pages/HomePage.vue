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
        class="col-3 p-5 mt-5 text-primary mainfont bg-dark"
      >
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore, quasi.
        Accusamus perspiciatis eligendi et similique consequuntur! Rem, eius
        sint saepe voluptatem dolor delectus natus error aut blanditiis quis
        quae omnis quia aliquam harum similique quod distinctio asperiores.
        Tempora perspiciatis non dignissimos accusantium! Qui, animi facilis sed
        alias culpa necessitatibus reiciendis consectetur, eligendi facere
        accusamus accusantium cumque similique delectus libero natus? Impedit,
        dolorem, debitis facilis maiores aliquam ratione facere molestiae eos,
        nesciunt quisquam alias eligendi. Fugiat, quae dolore voluptatum,
        tempora error maiores, tenetur doloremque perferendis quasi quibusdam
        atque deserunt sit commodi molestias labore officiis similique dolorum?
        Eligendi qui fugiat quis nobis delectus commodi minima veniam, dolore
        iure, atque odio perferendis earum exercitationem dolorem voluptatem vel
        pariatur nihil doloribus unde.
      </div>
    </div>
    <div id="portfolio"></div>
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
  --size: 20vmin;
  position: fixed;
  top: 50%;
  left: 50%;
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
