<template>
  <div>
    <pagination v-model="page" :records="500" :per-page="25"
                @paginate="myCallback" :options="options">
    </pagination>
    text
  </div>
</template>

<script>
import Pagination from 'v-pagination-3';
import MyPagination from "./MyPagination";

export default {
  name: 'Articles',
  data() {
    return {
      page: 1,
      options: {
        theme: 'bootstrap4',
        template: MyPagination
      }
    }
  },
  components: {
    Pagination
  },
  methods: {
    myCallback() {
      console.log(this.page);
    },
    setPage(page){
     console.log('setPage' + page)
    }
  }
}
</script>
