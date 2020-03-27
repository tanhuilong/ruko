<template>
  <div class="hello">
  <ul>
    <li><a href="#"><img src="../../public/img/menu_icon_gzt.png"><span> 业绩管理</span><i class="el-icon-arrow-down
 el-icon--right"></i></a>
 <ul><li @click="menu1"><a href="#">业绩报表</a></li></ul>
 </li>
    <li><a href="#"><img src="../../public/img/menu_icon_yygl.png"> 运营管理<i class="el-icon-arrow-down
 el-icon--right"></i></a></li>
    <li><a href="#"><img src="../../public/img/menu_icon_xt.png"> 系统管理<i class="el-icon-arrow-down
 el-icon--right"></i></a>
 <ul>
   <li><a href="#">用户管理</a></li>
   <li @click="menu2"><a href="#">角色权限管理</a></li>
 </ul>
 </li>
  </ul>
  </div>
</template>
<script>
export default {
  methods:{
    menu1(){
      
    },
    menu2(){
      
    }
  }
}
</script>


<style scoped lang="less">

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
}
a {
  display: block;
  width:170px;
  color: #fff;
  height: 40px;
  text-align: center;
  line-height: 40px;
}
.hello li ul{
  display: none;
}
.hello li a:hover,.hello li ul li a:hover{
  background: red;
}
.hello li:hover ul{
  display: block;
}
</style>
