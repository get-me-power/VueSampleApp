<template>
<div>
    <counter></counter>
    <div>Hello{{ user.name }}</div>
    <div>Hello{{ user.age }}</div>
    <!-- 三項演算子を理解しような -->
    <div>{{todo.name}}</div>
    <input type='text' :value="todo.name">
    <div>{{todo.name.length>= 20 ? '文字数を減らしてください': ''}}</div>
</div>
</template>

<script>
import Count from "./Count";
export default {
  name: 'HelloWorld',
  components: {
    //counterというdom(コンポーネント)を作る
    counter: Count 
  },
  data () {
    return {
      user: {
        name: 'Kouzi Tadokoro',
        age: 24
      },
      todo: {
        name: "無駄無駄無駄無駄無駄無駄無駄無駄無駄無駄無駄無駄無駄無駄"
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>