<template>
  <ag-grid-vue
    style="height: 460px; width: 1140px"
    class="ag-theme-material"
    :columnDefs="columnDefs"
    :rowData="rowData"
    :defaultColDef="defaultColDef"
  ></ag-grid-vue>
</template>

<script>
import { AgGridVue } from "ag-grid-vue";

export default {
  name: "AgGrid",
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
  data () {
    return {
      defaultColDef: {
        resizable: true,
        sortable: true,
        filter: true,
      },
    };
  },
};
</script>
