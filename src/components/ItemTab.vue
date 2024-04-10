<script setup>
import ItemTable from "@/components/TableComponents/ItemTable.vue";

import {reactive} from "vue";

const rows = reactive( [
  {
    name: 'Chicken Nuggets',
    quantity: 2,
    type: 'Bags',
    favorite: 'Favorite!'
  },
  {
    name: 'Ground Beef',
    quantity: 1,
    type: 'pounds',
    favorite: ' '
  },
  {
    name: 'Ice Cream',
    quantity: 4,
    type: 'Singles',
    favorite: 'Favorite!'
  },
  {
    name: 'Frozen Mango Chunks',
    quantity: 3,
    type: '5oz bags',
    favorite: ' '
  }
])
</script>

<template>
  <div class="tab-pane fade show active" id="item-tab-pane" role="tabpanel" aria-labelledby="item-tab" tabindex="0">
    <div class="container text-center" content="width=device-width, initial-scale=1">
      <item-table :rows="rows"></item-table>
    </div>
  </div>
</template>

<style scoped>

</style>