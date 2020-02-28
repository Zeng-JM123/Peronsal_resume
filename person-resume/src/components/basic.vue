<template>
  <div class="basic">
    <h2 class="title">基础信息</h2>
    <img class="head" src="../assets/images/timg.gif" alt="">
    <p class="info" v-for="(info, index) in infomation" :key="index">{{info.value}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      infomation: [
        {value: '姓名：曾佳铭'},
        {value: '性别：男'},
        {value: '年龄：20'},
        {value: '健康状况：良好'},
        {value: '籍贯：广东汕头'},
        {value: '所在学校：重庆交通大学'},
        {value: '当前年级：大三'},
        {value: '专业：能源与动力工程'},
        {value: '联系方式（QQ）：399702236'},
        {value: '求职意向：Web前端开发工程师'},
      ]
    }
  }
}
</script>

<style lang="scss">
.basic{
  width: 100%;
  height: 100%;
  position: relative;
  .title{
    padding: 18px 0 8px 20px;
  }
  .info{
    padding: 3px 0 3px 20px;
  }
  .head{
    width: 140px;
    height: 150px;
    position: absolute;
    top: 0;
    left: 140px;
  }
}
</style>