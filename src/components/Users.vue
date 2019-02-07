<template>
  <div class="users">
    <h1>Vue 组件嵌套Demo</h1>
    <ul>
        <li v-for="user in users" v-on:click="user.show=!user.show">
          <h2>{{user.name}}</h2>
          <h3 v-show="user.show">{{user.position}}</h3>
        </li>
    </ul>  
  </div>
</template>

<script>
export default {
  name: 'users',
  data () {
    return {
     users:[
       {name:"诸葛亮",position:"军师",show:false},
       {name:"刘备",position:"主公",show:false},
       {name:"关羽",position:"战士",show:false},
       {name:"张飞",position:"坦克",show:false},
       {name:"貂蝉",position:"法师",show:false},
       {name:"吕布",position:"战士",show:false}
       ]
    }
  }
}
</script>


<style scoped>
*{
  transition: all 0.2s
}
h1{
  text-align: center;
}
.users{
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}
ul{
  display: flex;
  flex-wrap: wrap;
  list-style-type: none ;
  padding: 0;
}
li{
  flex-grow: 1;
  flex-basis: 200px;
  text-align: center;
  padding: 30px;
  border: 1px solid  #222;
  margin: 10px;
}
</style>
