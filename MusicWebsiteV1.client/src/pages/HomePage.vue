<template>
  <div class="container-fluid">
    <div style="z-index: 1" class="cube-wrap parallax">
      <div style="z-index: 1" class="cube">
        <div
          style="z-index: 1"
          class="side top border pulse border-white"
        ></div>
        <div
          style="z-index: 1"
          class="side bottom border pulse border-white"
        ></div>
        <div
          style="z-index: 1"
          class="side front border pulse border-white"
        ></div>
        <div
          style="z-index: 1"
          class="side back border pulse border-white"
        ></div>
        <div
          style="z-index: 1"
          class="side left border pulse border-white"
        ></div>
        <div
          style="z-index: 1"
          class="side right border pulse border-white"
        ></div>
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
      <div class="row mt-5 justify-content-end">
        <div class="circle justify-content-center col-5">
          <img
            class="img-fluid"
            id="mandala"
            src="src\assets\img\Recurso 9MANDALA.svg"
            alt="scroll"
          />
        </div>

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

        <div class="p-5"></div>
        <div class="p-5"></div>
        <div class="p-5"></div>
      </div>
    </div>
  </div>
  <div style="z-index: 0" class="container-fluid parallax2"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
  <div class="p-5"></div>
</template>


<script>

export default {

  name: 'Home',
}
//cube rotate
window.addEventListener('scroll', () => {
  document.body.style.setProperty('--scroll', window.pageYOffset / (document.body.offsetHeight - window.innerHeight));
}, false);

window.onscroll = function () {
  scrollRotate();
};


//scroll spin
function scrollRotate() {
  let image = document.getElementById("mandala");
  image.style.transform = "rotate(" + window.pageYOffset / 1.61803398875 + "deg)";
}


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
.parallax2 {
  background-image: url("../assets/img/matrix.gif");
  height: 100vh;
  width: 100%;
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

.cube-wrap {
  --size: 33vmin;
  position: fixed;
  top: 55%;
  left: 66%;
  width: 0;
  height: 0;
  perspective: 100vmin;
}
.cube {
  transform-style: preserve-3d;
  transform: rotateX(100deg) rotateZ(45deg) rotateY(-45deg);
  animation: cube 7s linear;
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
.pulse {
  filter: drop-shadow(0px 10px 10px rgba(61, 255, 54, 0.055));
  animation: pulsate 2s ease-in-out infinite;
}
@keyframes pulsate {
  0% {
    filter: drop-shadow(0px 0px 5px rgba(100, 255, 100, 0.111));
  }
  10% {
    filter: drop-shadow(0px 0px 4.8px rgba(100, 248, 100, 0.222));
  }
  15% {
    filter: drop-shadow(0px 0px 5.2px rgba(100, 255, 100, 0.333));
  }
  25% {
    filter: drop-shadow(0px 0px 5.4px rgba(90, 255, 90, 0.444));
  }
  35% {
    filter: drop-shadow(0px 0px 5.6px rgba(90, 255, 90, 0.555));
  }
  45% {
    filter: drop-shadow(0px 0px 5.4px rgba(80, 255, 80, 0.666));
  }
  50% {
    filter: drop-shadow(0px 0px 5.8px rgba(80, 255, 80, 0.777));
  }
  60% {
    filter: drop-shadow(0px 0px 5.2px rgba(90, 255, 90, 0.666));
  }
  65% {
    filter: drop-shadow(0px 0px 5.4px rgba(90, 255, 90, 0.555));
  }
  75% {
    filter: drop-shadow(0px 0px 5.8px rgba(100, 255, 100, 0.444));
  }
  85% {
    filter: drop-shadow(0px 0px 5.4px rgba(100, 255, 100, 0.333));
  }
  95% {
    filter: drop-shadow(0px 0px 5px rgba(100, 255, 100, 0.222));
  }
  100% {
    filter: drop-shadow(0px 0px 5.2px rgba(100, 255, 100, 0.111));
  }
}

.circle {
  border-radius: 50%;
  width: 100px;
  height: 100px;
  display: table-cell;
}
#mandala {
  width: 100px;
  height: 100px;
}
</style>
