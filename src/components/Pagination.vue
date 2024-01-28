<!-- src/components/Pagination.vue -->

<template>
    <div class="pagination">
      <button v-for="page in totalPages" :key="page" @click="changePage(page)">
        {{ page }}
      </button>
    </div>
</template>
  
  <script>
  export default {
    props: {
      data: {
        type: Array,
        required: true,
      },
    },
    computed: {
      totalPages() {
        return Math.ceil(this.data.length / this.perPage);
      },
    },
    methods: {
      changePage(page) {
        this.$emit('pagination-change-page', page);
      },
    },
  };
  </script>
  
  <style scoped>
  .pagination {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
  }
  
  .pagination button {
    margin: 0 5px;
    padding: 5px 10px;
    cursor: pointer;
  }
  </style>
  