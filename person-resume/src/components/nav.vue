<template>
  <div class="nav">
    <div class="logo"><img v-show="isShowImg" src="../assets/images/logo1.png" alt="logo"><img v-show="!isShowImg" src="../assets/images/logo2.png" alt="logo"></div>
    <div class="title">铭铭的线上简历</div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      isShowImg: true
    }
  },
  mounted(){
    setInterval(() => {
      this.isShowImg = !this.isShowImg;
    }, 5000);
  }
}
</script>

<style lang="scss">
  .nav{
    width: 100%;
    height: 100%;
    background-color: #888;
    .logo{
       float: left;
      margin-left: 20px;
      width: 100px;
      height: 75px;
      position: relative;
      img{
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        animation: imgIn 5s infinite;
      }
      @keyframes imgIn {
        0%{
          top: -75px;
          left: 0;
        }
        20%{
          top: 0;
          left: 0;
        }
        80%{
          top: 0;
          left: 0;
        }
        100%{
          top: 0;
          left: 100px;
        }
      }
    }
    .title{
      display: inline-block;
      padding: 0 60px;
      // background-color: #38f;
      background-color: #555;
      opacity: 0.9;
      z-index: 100;
      color: white;
      height: 75px;
      line-height: 75px;
      font-size: 21px;
      margin-left: 20px;
      font-weight: 550;
    }
  }
</style>