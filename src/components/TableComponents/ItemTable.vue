<script setup>
import {computed, onMounted, ref} from "vue";

const props = defineProps( {
  rows: {
    type: Object,
    required: true
  }
})

const shallowRows = ref( [...props.rows])

const headerItems = computed( () => {
  return Object.keys(props.rows[0])
})

const sortData = (sortBy, direction) => {
  switch (sortBy) {
    case 'quantity' :
      shallowRows.value = shallowRows.value.sort( (a,b) => {
        return (direction === 'ASC' ? a : b )[sortBy] - (direction === 'ASC' ? b : a )[sortBy]
      })
      break
    default :
      shallowRows.value = shallowRows.value.sort( (a,b) => {
        return (direction === 'ASC' ? a : b )[sortBy].localeCompare((direction === 'ASC' ? b : a )[sortBy])
      })
  }
}
</script>

<template>
  <h1>Here's a list of items!</h1>
  <div class="table-header">
    <div class="table-header__item" v-for="item in headerItems" :key="item">
      <p> {{item.toUpperCase()}}</p>
      <button @click="sortData(item, 'ASC')">Asc</button>
      <button @click="sortData(item, 'DESC')">Dsc</button>
    </div>
  </div>
  <div class="table-row" v-for="(row, index) in shallowRows" :key="index">
    <div class="table-column__item" v-for="column in Object.values(row)" :key="column">
      {{ column }}
    </div>
  </div>
</template>

<style scoped>
.table-row,
.table-header {
  display: flex;
  flex-wrap: nowrap;
}

.table-header__item,
.table-column__item {
  width: 25%;
  border: solid 1px #4d4d4d;
  padding: 8px 16px;
  box-sizing: border-box;
}
</style>