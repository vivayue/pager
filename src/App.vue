<template>
  <div id="app">
    <paging 
      :page-size="pagesize"
      :page-count="pageCount"
      :total.sync="total"
      :current.sync="current"
      @change="changePage"/>
  </div>
</template>

<script>
import paging from './components/paging.vue'

export default {
  name: 'app',
  components: {
    paging
  },
  data() {
    return {
      current: 1, // 当前页
      open: false,
      total:150, // 总记录数
      pagesize: 15, // 一页多少条
      pageCount: 7 // 页码按钮的数量，当总页数超过该值时会折叠
    };
  },
  methods:{
    changePage(e) {
      console.log(e);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
