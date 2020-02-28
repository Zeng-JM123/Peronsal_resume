<template>
  <div class="bubble_demo">
    <div class="title">个人标签</div>
    <canvas id="myCanvas"></canvas>
  </div>
</template>

<script>
export default {
  methods: {
    init () {
      var myCanvas = document.getElementById('myCanvas');
      var ctx = myCanvas.getContext('2d');
      ctx.font = '11px bold 黑体';
      ctx.globalAlpha = 0.8;
      var tagList = ['阳光', '乐观', '奋斗', '吃货', '学习', '追求', '民谣', '努力', '吉他', '死磕'];
      class Bubble {
        constructor(x, speedX, speedY) {
          this.fontText = tagList[Math.ceil(Math.random()*9)];
          this.x = x;
          this.y = 320;
          this.color = renderColor();
          this.speedX = speedX * Math.random() - 0.5;
          this.speedY = speedY;
          this.render()
        }
        render () {
          ctx.beginPath();
          ctx.fillStyle = `${this.color}`;
          ctx.ellipse(this.x, this.y-180, 24, 18, 0, Math.PI / 2, 2.5 * Math.PI);
          ctx.fill()
          ctx.beginPath()
          ctx.bezierCurveTo(this.x+3, this.y-161, this.x+23, this.y-155, this.x+5, this.y-145)
          ctx.bezierCurveTo(this.x+5, this.y-145, this.x-15, this.y-135, this.x, this.y-128)
          ctx.stroke()
          ctx.fillStyle = 'black';
          ctx.fillText(this.fontText, this.x-11, this.y-176)
          this.run()
        }
        run () {
          this.x += this.speedX;
          this.y -= this.speedY;
        }
      };
      var bubbleArr = []

    for(let i = 0; i < 5500; i++){
      (function(){
        setTimeout(getBubble, 2000*i);
      })()
    }

    function getBubble(){
      var bubble = new Bubble(Math.random()*myCanvas.width,1,0.6);
      bubbleArr.push(bubble);
    }
    

    setInterval(() => {
      ctx.clearRect(0,0,1000,1000)
      bubbleArr.forEach(function(ele, index){
        ele.render()
      })
    }, 16);
    function renderColor(){
      return 'rgb(' + parseInt(Math.random()*255) + ',' + parseInt(Math.random()*255) + ',' + parseInt(Math.random()*255) + ')' ;
    }

    },
  },
  mounted () {
    this.init()
  }
}
</script>

<style lang="scss">
.bubble_demo {
  width: 100%;
  height: 100%;
  background-color: #333;
  .title{
    height: 38px;
    width: 150px;
    background-color: #eeb;
    position: absolute;
    font-size: 18px;
    font-weight: 550;
    line-height: 38px;
    text-align: center;
    box-shadow: #000 2px 2px 3px;
    // margin: 1px;
  }
  #myCanvas {
    width: 100%;
    height: 100%;
  }
}
</style>