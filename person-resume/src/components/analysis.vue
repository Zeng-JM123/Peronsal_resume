<template>
  <div class="analysis">
    <nightingale class="analysis-table"/>
  </div>
</template>

<script>
import nightingale from './echarts/nightingale.vue'
export default {
  components: {
    nightingale
  }
}
</script>

<style lang="scss">
.analysis{
  display: inline-block;
  width: 100%;
  height: 100%;
  .analysis-table{
    width: 100%;
    height: 100%;
  }
}
</style>