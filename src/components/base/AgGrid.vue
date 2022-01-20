<template>
  <ag-grid-vue
    style="height:460px; width:1140px"
    class="ag-theme-material"
    :columnDefs="columnDefs"
    :rowData="rowData"
  ></ag-grid-vue>
</template>

<script>
import { AgGridVue } from 'ag-grid-vue';

export default {
  name: 'AgGrid',
  components: {
    AgGridVue,
  },
  props: {
    columnDefs: {
      type: Array,
      required: true,
    },
    rowData: {
      type: Array,
      required: true,
    },
  },
};
</script>
