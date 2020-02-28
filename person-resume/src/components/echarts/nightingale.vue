<template>
  <div id="char"></div>
</template>

<script>
import echarts from 'echarts';
export default {
  data(){
    return {
      options: {
        title: {
          text: '个人技能分析',
          left: 'center'
        },
        legend: {
          show: true,
          left: 'left',
          itemGap: 14,
          align: 'auto',
          orient: 'vertical',
          data: ['CSS3', 'HTML5', 'Vue', 'jQuery', 'nodeJs', 'http', 'JavaScript', '其他'],
          textStyle: {
            fontSize: 13
          }
        },
        tooltip: {
          trigger: 'item',
          formatter: '{a} <br/>{b} : {c} ({d}%)'
        },
        series: [
          {
            name: '个人技能',
            type: 'pie',
            roseType: 'area',
            radius: [30, 110],
            data: [
              { value: 16, name: 'CSS3'},
              { value: 18, name: 'HTML5' },
              { value: 25, name: 'Vue' },
              { value: 15, name: 'jQuery' },
              { value: 17, name: 'nodeJs' },
              { value: 20, name: 'http' },
              { value: 25, name: 'JavaScript' },
              { value: 10, name: '其他' }
            ]
          }
        ]
      }
    }
  },
  methods: {
    setEcharts () {
      var myChart = echarts.init(document.getElementById('char'));
      // console.log(myChart)
      myChart.setOption(this.options)
    }
  },
  mounted () {
    this.setEcharts();
  }
}
</script>

<style lang="scss">
</style>