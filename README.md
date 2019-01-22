# mypager(基于vue2.0的翻页组件)

## 如何使用？
1、注册组件
```
  import paging from "@vivayue/viva-paging"
  // 引入样式
  import "@vivayue/viva-paging/dist/viva-paging.css";
  Vue.component(paging.pager.name, paging.pager);
```
2、页面使用该组件
```
<paging :page-size="pagesize" :page-count="pageCount" :total.sync="total" :current.sync="current" @change="changePage"></paging>
```
3、参数说明
参数      | 默认值(type)| 描述
----------|------------|-------------------------------------
current   | 1(number)  | 当前页
total     | 0(number)  | 总记录数
pagesize  | 15(number) | 一页多少条
pageCount | 7(number)  | 页码按钮的数量，当总页数超过该值时会折叠

dog | bird | cat
----|------|----
foo | foo  | foo
bar | bar  | bar
baz | baz  | baz

3、调用方法
```
methods:{
  changePage(e) {
    console.log(e);
  }
}
```
## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
