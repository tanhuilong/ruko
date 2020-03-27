<template>
    <div class="lie">
        <div class="l-top">
    <el-row :gutter="10">
  <el-col :span="2"><div class="grid-content bg-purple">序号</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">地区公司</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">邀请注册</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">分享海报</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">客户浏览</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">已推荐</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">已到访</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">已认购</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">已签到</div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple">操作</div></el-col>
</el-row>
</div>
<div class="l-mid" >
    <el-row :gutter="10">
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.num}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.place}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.share}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.sharesea}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.scan}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.tui}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.fang}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.gou}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.qian}}</li></div></el-col>
  <el-col :span="2"><div class="grid-content bg-purple"><li v-for="(item,index) in list" :key="index">{{item.op}}</li></div></el-col>
</el-row>
</div>
<div class="l-footer">
    <el-pagination
  background
  layout="prev, pager, next"
  :total="1000">
</el-pagination>
</div>
    </div>
</template>
<script>
export default {
    data(){
       var _this=this;
       var url="json/lie.json";
       this.$http.get(url).then(res=>{
           _this.list=res.data
       })
       return{
           list:[]
       }
        
    },
    methods:{
                   
    }
}
</script>
<style >
.l-top{
    height: 40px;
    color: #fff;
    margin:10px 0 0 10px;

}
.l-mid{
    margin-left: 10px;
}
.el-col div {
    font-size: 14px;
}
li{
    list-style: none;
    height: 30px;
}
.l-footer{
   text-align: center;
}
</style>