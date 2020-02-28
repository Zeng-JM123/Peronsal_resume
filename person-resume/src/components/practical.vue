<template>
  <div class="practical_wrap">
    <h2 class="title">实习经历</h2>
    <p class="duration">{{duration}}</p>
    <p class="company">{{company}}</p>
    <p class="content">{{content}}</p>
    <p class="about"><b>关于这个简历：</b>{{about_content}}</p>
    <p class="thanks">{{thanks}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return {
      duration: '2020.01.13~2020.02.09',
      company: '广州XXX科技有限公司',
      content: '我参与了XXX后台管理系统项目，主要负责写静态页面，以及熟悉公司开发项目流程，本次项目前端部分使用的是vue-cli+elementUI，本次实习使对我模块化开发有了很好的理解以及进一步熟悉elementUI组件库的运用。',
      about_content: '该项目内容基于自身情况，关于简历的布局灵感，部分来自于网上，如果有冒犯之处还望您提出，我会第一时间做出改正！',
      thanks: '再一次感谢您宝贵的时间，希望能够得到您的反馈！'
    }
  }
}
</script>

<style lang="scss">
.practical_wrap{
  width: 100%;
  height: 100;
  .duration{
    float: right;
    padding: 10px 10px 0 0;
  }
  .title{
    padding: 15px 0 5px 20px;
  }
  .company{
    padding: 5px 0 5px 20px;
    font-size: 15px;
  }
  .content{
    padding: 5px 0 5px 20px;
  }
  .about{
    margin: 10px 20px 0;
    border-top: 1px solid #999;
    padding: 10px 0 0;
  }
  .thanks{
    padding: 5px;
    text-align: center;
    font-size: 15px;
    font-family: "Times New Roman";
  }
}
</style>