<template>
  <div class="expression_wrap">
    <h2 class="title">在校表现</h2>
    <p class="info" v-for="(info, index) in infoList" :key="index">{{info.value}}</p>
    <p class="person_evaluation"><b>个人评价: </b>{{evaluation_content}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      infoList: [
        {value: '2019年全国大学生数学建模大赛重庆市二等奖'},
        {value: '2018年全国大学生数学竞赛校一等奖'},
        {value: '大学生创新创业大赛校三等奖'},
        {value: '大学生英语四级证书'},
        {value: '计算机二级MS Office二级证书'},
      ],
      evaluation_content: '对于我这个工科学生来说，跨专业真的好难啊，学习前端一路坎坷，前端是我要努力的方向，这一路上我发现了自己也有那种不服输的精神，一定要坚持把这件事情做好，我会继续死磕到底！',
    }
  }
}
</script>

<style lang="scss">
.expression_wrap{
  width: 100%;
  height: 100%;
  .title{
    padding: 10px 0 5px 20px;
  }
  .info{
    padding: 2px 0 2px 20px;
  }
  .person_evaluation{
    margin: 20px;
    padding: 10px 0;
    margin-top: 5px;
    border-top: 1px solid #999;
  }
}
</style>