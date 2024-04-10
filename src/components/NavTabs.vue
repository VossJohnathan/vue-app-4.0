<script setup>
import ItemTab from "@/components/ItemTab.vue";
import InfoTab from "@/components/InfoTab.vue";
import InfoTable from "@/components/TableComponents/InfoTable.vue";
import ItemTable from "@/components/TableComponents/ItemTable.vue";
</script>

<template>
  <div id="myNavTabs">
    <ul class="nav nav-tabs nav-fill mb-3" id="myTab" role="tablist">
      <li class="nav-item" role="presentation">
        <button class="nav-link active" id="item-tab" data-bs-toggle="tab" data-bs-target="#item-tab-pane" type="button" role="tab" aria-controls="item-tab-pane" aria-selected="true">List of Items</button>
      </li>
      <li class="nav-item" role="presentation">
        <button class="nav-link" id="info-tab" data-bs-toggle="tab" data-bs-target="#info-tab-pane" type="button" role="tab" aria-controls="info-tab-pane" aria-selected="false">Item Info</button>
      </li>
    </ul>
  </div>

  <div class="tab-content">
    <div class="tab-pane fade show active" id="item-tab-pane" role="tabpanel" aria-labelledby="item-tab" tabindex="0">
      <item-tab></item-tab>
    </div>
    <div class="tab-pane fade" id="info-tab-pane" role="tabpanel" aria-labelledby="info-tab" tabindex="0">
      <info-tab></info-tab>
    </div>
  </div>

</template>

<style scoped>
  .nav-link.active {
    color: white;
    background-color: #048BA8;
  }

  .nav-link {
    color: white;
    background: #635D5C;
  }
</style>