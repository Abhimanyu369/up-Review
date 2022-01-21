<template>
  <div class="ma-2">
    <ag-grid :columnDefs="columnDefs" :rowData="rowData"></ag-grid>
  </div>
</template>

<script>
import AgGrid from "@/components/base/AgGrid.vue";
import reviewData from "@/assets/reviewData.json";

export default {
  name: "ReviewTable",
  components: {
    AgGrid,
  },
  data() {
    return {
      columnDefs: [],
      rowData: [],
    };
  },
  watch: {
    rowData(data) {
      this.rowData = data;
    },
  },
  methods: {},
  beforeMount() {
    this.columnDefs = [
      {
        headerName: "Reviewer Id",
        field: "reviewerID",
        filter: "agTextColumnFilter",
      },
      { headerName: "Asin", field: "asin", filter: "agTextColumnFilter" },
      {
        headerName: "Reviewer Name",
        field: "reviewerName",
        filter: "agTextColumnFilter",
      },
      {
        headerName: "Review Text",
        field: "reviewText",
        filter: "agTextColumnFilter",
      },
      { headerName: "Helpful", field: "helpful", filter: "agTextColumnFilter" },
      { headerName: "Overall", field: "overall", filter: "agTextColumnFilter" },
      { headerName: "Summary", field: "summary", filter: "agTextColumnFilter" },
      {
        headerName: "Review Time",
        field: "reviewTime",
        filter: "agTextColumnFilter",
      },
    ];
    this.rowData = reviewData;
  },
};
</script>
