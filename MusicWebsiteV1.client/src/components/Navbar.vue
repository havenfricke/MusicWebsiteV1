<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark px-3">
    <router-link class="navbar-brand d-flex" :to="{ name: 'Home' }">
      <div class="d-flex flex-column align-items-center">
        <img
          class="rounded-circle hoverable"
          alt="logo"
          src="src\assets\img\Recurso 31MANDALA.svg"
          height="60"
        />
      </div>
    </router-link>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarText"
      aria-controls="navbarText"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <ul class="navbar-nav me-auto">
        <li>
          <router-link
            :to="{ name: 'About' }"
            class="btn text-success lighten-30 selectable text-uppercase"
          >
            About
          </router-link>
          <router-link
            :to="{ name: 'About' }"
            class="btn text-success lighten-30 selectable text-uppercase"
          >
            About
          </router-link>
          <router-link
            :to="{ name: 'About' }"
            class="btn text-success lighten-30 selectable text-uppercase"
          >
            About
          </router-link>
        </li>
      </ul>
      <span class="col-10">
        <img
          class="pulse"
          src="src\assets\img\Recurso 15MODERN ICON.svg"
          alt=""
        />
      </span>
      <!-- LOGIN COMPONENT HERE -->
      <Login hidden />
    </div>
  </nav>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped lang="scss">
a:hover {
  text-decoration: none;
}
.nav-link {
  text-transform: uppercase;
}
.navbar-nav .router-link-exact-active {
  border-bottom: 2px solid var(--bs-success);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}
.hoverable:hover {
  transform: scale(1.08);
  transform: rotate(360deg);
  filter: drop-shadow(0px 0px 15px rgb(63, 255, 98));
  transition: 500ms ease-in-out;
  cursor: pointer;
}
.hoverable:active {
  transform: scale(0.98);
  transition: 50ms ease-in-out;
}
img {
  transition: transform 0.7s ease-in-out;
}

.hoverable2:hover {
  filter: drop-shadow(0px 0px 5px rgb(63, 255, 98));
  transition: 500ms ease-in-out;
  cursor: pointer;
}
body {
  background: #000;
}
.pulse {
  filter: drop-shadow(0px 10px 10px rgb(9, 255, 0));
  animation: pulsate 3s ease-in-out infinite;
}
@keyframes pulsate {
  0% {
    filter: drop-shadow(0px 0px 5px rgba(9, 255, 0, 0.456));
  }
  25% {
    filter: drop-shadow(0px 0px 7px rgba(9, 255, 0, 0.882));
  }
  35% {
    filter: drop-shadow(0px 0px 5px rgba(9, 255, 0, 0.634));
  }
  50% {
    filter: drop-shadow(0px 0px 5px rgb(9, 255, 0));
  }
  75% {
    filter: drop-shadow(0px 0px 6px rgba(9, 255, 0, 0.814));
  }
  85% {
    filter: drop-shadow(0px 0px 5px rgba(9, 255, 0, 0.595));
  }
  100% {
    filter: drop-shadow(0px 0px 8px rgba(9, 255, 0, 0.456));
  }
}
</style>
