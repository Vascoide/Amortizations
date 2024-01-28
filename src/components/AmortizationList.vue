<!-- src/components/AmortizationList.vue -->

<template>
  <div>
    <h1>Amortization List</h1>
    <table class="table">
      <thead>
        <tr>
          <th @click="sort('schedule_date')">Schedule Date</th>
          <th @click="sort('state')">State</th>
          <th @click="sort('amount')">Amount</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="amortization in paginatedAmortizations" :key="amortization.id">
          <td>{{ amortization.schedule_date }}</td>
          <td>{{ amortization.state }}</td>
          <td>{{ amortization.amount }}</td>
        </tr>
      </tbody>
    </table>
    <Pagination :data="amortizations" @pagination-change-page="paginate" />
  </div>
</template>

<script>
import Pagination from "@/components/Pagination.vue";

export default {
  props: {
    components: {
      Pagination,
    },
    amortizations: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      sortedAmortizations: [],
      currentPage: 1,
      perPage: 10,
    };
  },
  computed: {
    paginatedAmortizations() {
      const start = (this.currentPage - 1) * this.perPage;
      const end = start + this.perPage;
      return this.sortedAmortizations.slice(start, end);
    },
  },
  methods: {
    sort(column) {
      this.sortedAmortizations = this.amortizations.sort((a, b) => {
        if (a[column] < b[column]) return -1;
        if (a[column] > b[column]) return 1;
        return 0;
      });
    },
    paginate(page) {
      this.currentPage = page;
    },
  },
};
</script>

<style scoped>
.table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

.table th, .table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

.table th {
  cursor: pointer;
  background-color: #f2f2f2;
}

.pagination {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.pagination button {
  margin: 0 5px;
  padding: 5px 10px;
  cursor: pointer;
}
</style>
