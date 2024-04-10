<script setup>
defineProps( {
  freezerWelcome: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="welcome">
    <h1 class="blue">{{ freezerWelcome }}</h1>
    <h3>
      ☃️❄️🥶Let's find out what's in <b>Your</b> Freezer! 🥶❄️☃️
    </h3>
    <hr style="border: 3px solid">
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.welcome h1,
.welcome h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .welcome h1,
  .welcome h3 {
    text-align: left;
  }
}
</style>