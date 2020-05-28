<template>
  <div class="echarts-container">
      <router-view class="echart-content"></router-view>
      <div class="echarts-footer">
          <div class="echarts-item">
              <router-link to="/home/echarts/lineechart" tag="span" active-class="echarts-item-active">折线</router-link>
          </div>
          <div class="echarts-item"> <router-link to="/home/echarts/barechart" tag="span" active-class="echarts-item-active">柱状</router-link></div>
          <div class="echarts-item"> <router-link to="/home/echarts/pieechart" tag="span" active-class="echarts-item-active">饼</router-link></div>
          <div class="echarts-item"> <router-link to="/home/echarts/radarechart" tag="span" active-class="echarts-item-active">雷达</router-link></div>
          <div class="echarts-item"> <router-link to="/home/echarts/sunburstechart" tag="span" active-class="echarts-item-active">旭日</router-link></div>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    created(){
        // console.log(this.$root._route.path == '/home/echarts/lineechart'?'#04f':'#555',this.$root._route.path== '/home/echarts/lineechart',this.$root._route.path)
    }
}
</script>

<style scoped>

    .echarts-container{
        height: 100%;
        position: relative;
    }
    .echart-content{
        height: calc(100% - 1rem);
    }
    .echarts-footer{
        position:absolute;
        bottom: 0;
        border-top:1px solid #999;
        width: 100%;
        font-size: 0.5rem;
        height: 1rem;
        display: flex;
        line-height: 1rem;
        justify-content: space-between;
    }
    .echarts-item{
        background-color: #eee;
        padding:0 0.51rem;
        border-right: 1px solid #999;
        border-left: 1px solid #999;
    }
    .echarts-item-active{
        color: #409EFF;
    }

</style>



