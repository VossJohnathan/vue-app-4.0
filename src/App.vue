<script setup>
//New imports go below.
import FreezerWelcome from "./components/FreezerWelcome.vue";
import FreezerMainPage from "./components/FreezerMainPage.vue";
</script>

<template>
  <header>
    <img class="logo" src="./assets/What's%20in%20that%20freezer.png" width="750" height="250" />

    <div class="wrapper">
      <FreezerWelcome freezer-welcome="What's In That Freezer?!" />
    </div>
  </header>

  <main>
    <freezer-main-page />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}


@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
