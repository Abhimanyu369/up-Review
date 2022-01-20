<template>
  <div class="ma-2">
    <ag-grid :columnDefs='columnDefs' :rowData='rowData' ></ag-grid>
  </div>
</template>

<script>
import AgGrid from '@/components/base/AgGrid.vue';
import reviewData from '@/assets/reviewData.json';

export default {
  name: 'ReviewTable',
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
        headerName: 'Reviewer Id',
        field: 'reviewerID',
      },
      { headerName: 'asin', field: 'asin' },
      { headerName: 'Reviewer Name', field: 'reviewerName' },
      { headerName: 'Review Text', field: 'reviewText' },
      { headerName: 'Helpful', field: 'helpful' },
      { headerName: 'Overall', field: 'overall' },
      { headerName: 'Summary', field: 'summary' },
      { headerName: 'Review Time', field: 'reviewTime' },
    ];
    console.log(reviewData);
    this.rowData = reviewData;
  },
};
</script>
