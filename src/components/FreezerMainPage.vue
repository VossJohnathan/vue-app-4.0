<script setup>
//Bootstrap Stuffs
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.js';

//importing other components
import NavTabs from "@/components/NavTabs.vue";
import ItemTab from "@/components/ItemTab.vue";
import InfoTab from "@/components/InfoTab.vue";

</script>

<template>
  <div class="mainPage">
    <h3>👇 We have two amazing sections to choose from! 👇</h3>
  </div>
  <div>
    <nav-tabs></nav-tabs>
    <!--Issue here. Because the tabs are both here, it places the info tab lower on the screen.-->
    <!-- Possible fix could be placing both tabs into the nav component. -->
    <!-- https://www.w3schools.com/bootstrap/bootstrap_tabs_pills.asp Toggleable / Dynamic Tabs -->

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

.mainPage h1,
.mainPage h3 {
  text-align: center;
}



@media (min-width: 1024px) {
  .mainPage h1,
  .mainPage h3 {
    text-align: left;
  }
}
</style>