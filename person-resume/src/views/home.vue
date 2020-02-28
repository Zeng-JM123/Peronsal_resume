<template>
  <div class="home">
    <div class="navigator">
      <Nav/>
    </div>
    <div class="container">
      <div class="top-wrap">
        <div class="basic box">
          <Basic/>
        </div>
        <div class="analysis box">
          <Analysis />
        </div>
        <div class="bubble box">
          <Bubble/>
        </div>
      </div>
      <div class="bottom-wrap">
        <div class="expression box">
          <Expression/>
        </div>
        <div class="practical box">
          <Practical/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Analysis from '../components/analysis'
import Basic from '../components/basic'
import Nav from '../components/nav'
import Bubble from '../components/bubble'
import Loading from '../components/loading'
import Expression from '../components/expression'
import Practical from '../components/practical'
export default {
  components: {
    Analysis,
    Basic,
    Bubble,
    Nav,
    Expression,
    Practical
  }
}
</script>

<style lang="scss">
.home {
  width: 100%;
  height: 100%;
  .navigator {
    width: 100%;
    height: 75px;
    .nav-wrap {
      width: 100%;
      height: 75px;
      .logo {
        width: 15%;
        height: 100%;
      }
    }
  }
  .container {
    height: calc(100% - 70px);
    .top-wrap {
      width: 100%;
      height: 320px;
      display: flex;
      justify-content: space-around;
      margin: 10px 0;
    }
    .box {
      background: white;
      height: 100%;
      display: inline-block;
    }
    .basic {
        width: 280px;
      }
      .analysis {
        width: 600px;
      }
      .bubble {
        width: 420px;
      }
    .bottom-wrap {
      width: 100%;
      display: flex;
      justify-content: space-around;
      .expression, .practical{
        width: 480px;
        height: 240px;
      }
    }
  }
}
</style>

