<template>
  <div class="home">
    <el-container class="wrapper">
      <el-header>
        <div>
          <img src="../assets/images/DSC.jpg" /> ZHANGHONG
        </div>

        <el-dropdown @command="getActiveMenue">
          <span class="el-dropdown-link">
            菜单
            <i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown" style=" left:7rem;top:0.75rem;">
            
            <el-dropdown-item command="/home/calculator">计算器</el-dropdown-item>
            <el-dropdown-item command="/home/echarts">图表</el-dropdown-item>
            <el-dropdown-item command="/home/circleNav">导航菜单</el-dropdown-item>
            <el-dropdown-item command="/home/queryweather">查询天气</el-dropdown-item>
            <el-dropdown-item command="/home/stock">旋转股子</el-dropdown-item>
            <el-dropdown-item command="/home/targettab">Tab选项卡</el-dropdown-item>
            <el-dropdown-item command="/home/swiper">轮播</el-dropdown-item>
            <el-dropdown-item command="/home/carousel">旋转木马</el-dropdown-item>
            <el-dropdown-item command="/home/taichi">太极图</el-dropdown-item>
            <el-dropdown-item command="/home/pie">饼图</el-dropdown-item>
            <el-dropdown-item command="/home/turnbook">翻书</el-dropdown-item>
            
            <el-dropdown-item command="/home/calendar">日历</el-dropdown-item>
            <el-dropdown-item command="/home/flashlamp">闪光灯</el-dropdown-item>
            
            
            
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>
      <el-container>
        
        <el-main over-flow="hidden" v-bind:style='{"height":winHeight*10/winWidth - 2.2 + "rem"}'>
          <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      winWidth:0,
      winHeight:0
    };
  },
  created() {
    this.getClientData()
  },
  methods: {
    getActiveMenue(index) {
      // console.log(index)
      this.$router.push({path:index})
    },
    getClientData(){
      this.winWidth=window.innerWidth;
      this.winHeight=window.innerHeight;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 1px;
}
a {
  color: #42b983;
  text-decoration: none;
}

.wrapper {
  margin-top: 10px;
}
.el-header {
  height: 2.2rem !important;
  color: #000;
  text-align: left;
  border-bottom: 1px solid #999;
  display: flex;
  font-size: 0.5rem;
}

.el-header img {
  height: 1.8rem;
  width: 1.8rem;
  border: 5px solid #fff;
  box-shadow: 1px 1px 10px #999;
  border-radius: 50%;
  vertical-align: middle;
  line-height: 1.8rem;
  margin-right: 20px;
}
.el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
.el-dropdown{
  width: 6rem;
  right: 0rem;
  /* border:1px solid #000; */
  top:1.3rem;
  height: 0.8rem;
  position: absolute;
  text-align: right;
  padding-right: 10px;
  font-size: 0.4rem;
}
.el-icon-arrow-down{
  font-size: 0.4rem;
}
.el-dropdown-menu{
  width: 30%;
  max-height: 10rem;
  overflow: auto;
  top:1rem
}
.el-popper[x-placement^=bottom]{
  margin-top:-1rem;
}
.el-dropdown-menu__item{
  padding: 0;
  text-align: center;
  width: 100%;
  font-size: 0.4rem;
}

/* width: 130px !important;
  background-color: #aaa;
}
.el-row {
  height: auto;
}*/
.el-main {
  padding: 1px;
}

/*
.el-menu-item {
  padding-left: 1px !important;
  height: 30px !important;
  line-height: 30px !important;
  font-size: 16px;
  border-bottom: 1px solid #eee;
  width: 95%;
} */
</style>
