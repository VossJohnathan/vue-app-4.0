<script setup>
import InfoTable from "@/components/TableComponents/InfoTable.vue";
import {reactive} from "vue";

const rows = reactive( [
  {
    name: 'Chicken Nuggets',
    expire: '6/24/2024',
    bought: '4/1/2024',
    store: 'Frozen Store'
  },
  {
    name: 'Ground Beef',
    expire: '4/28/2024',
    bought: '4/10/2024',
    store: 'Meat Store'
  },
  {
    name: 'Ice Cream',
    expire: '2/17/2025',
    bought: '13/15 44B.C.',
    store: 'Rome'
  },
  {
    name: 'Frozen Mango Chunks',
    expire: '8/12/2024',
    bought: '4/5/2024',
    store: 'The Mango Store'
  }
])

let date = new Date().toLocaleDateString();

</script>

<template>

    <div class="container text-center" content="width=device-width, initial-scale=1">
      <h1>Today's Date: {{ date }}</h1>
      <info-table :rows="rows"></info-table>
    </div>

</template>

<style scoped>

</style>