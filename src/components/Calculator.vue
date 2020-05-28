<template>
  <div style="overflow:hidden;">
      <div class="calculator">
        <div class="display">{{current || 0}}</div>
        <div class="button" @touchstart="clear">C</div>
        <div class="button" @touchstart='sign'>+/-</div>
        <div class="button" @touchstart="percent">%</div>
        <div class="button operator" @touchstart="divide">÷</div>
        <div class="button" @touchstart="append('7')">7</div>
        <div class="button" @touchstart="append('8')">8</div>
        <div class="button" @touchstart="append('9')">9</div>
        <div class="button operator" @touchstart="times">x</div>
        <div class="button" @touchstart="append('4')">4</div>
        <div class="button" @touchstart="append('5')">5</div>
        <div class="button" @touchstart="append('6')">6</div>
        <div class="button operator"  @touchstart="minus">-</div>
        <div class="button"  @touchstart="append('1')">1</div>
        <div class="button"  @touchstart="append('2')">2</div>
        <div class="button"  @touchstart="append('3')">3</div>
        <div class="button operator"  @touchstart="add">+</div>
        <div class="zero button"  @touchstart="append('0')">0</div>
        <div class="button"  @touchstart="dot">.</div>
        <div class="button operator" @touchstart="equal">=</div>
        
      </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      current:'',
      operator:null,
      previous:null,
      operatorClicked:false,
    }
  },
  methods:{
    clear(){
      this.current=''
    },
    sign(){
      // string.chartAt(index) 截取出字符串的第n个字符
      this.current=this.current.charAt(0) === '-' ?
        this.current.slice(1) : `-${this.current}`
    },
    percent(){
      this.current=`${parseFloat(this.current) / 100}`
    },
    append(number){
      if(this.operatorClicked){
        this.operatorClicked=false
        this.current=''
      }
      this.current=`${this.current + number}`
      
    },
    dot(){
      if(this.current.indexOf('.') === -1){
        this.append('.')
      }
    },
    setPrevious(){
      this.operatorClicked=true
      this.previous=this.current
    },
    divide(){
      this.operator=(a,b)=>a / b;
      this.setPrevious()
    },
    times(){
      this.operator=(a,b)=>a * b;
      this.setPrevious()
    },
    minus(){
      this.operator=(a,b)=>a - b;
     this.setPrevious()
    },
    add(){
      this.operator=(a,b)=>a + b;
      this.setPrevious()
    },
    equal(){
      this.current=`${ this.operator(parseFloat(this.previous),parseFloat(this.current))}`
      this.previous=null
    }
  }
}
</script>

<style scoped>
.calculator{
 display: grid;
 display: -moz-grid;
 display: -ms-grid;
 /* 设置每一行有多少列 */
 grid-template-columns: repeat(4,1fr);
 /* 设置行大小 */
 grid-auto-rows: minmax(1rem,auto);
 width: 7rem;
 margin:2rem auto;
}

.calculator>div{
  font-size: 0.4rem;
  line-height: 1rem;
}
.display{
  grid-column: 1 / 5;
  background-color: #333;
  color: #fff;
  font-size: 1rem !important;
  height: 1.5rem;
  line-height: 1.5rem !important;
}
.zero{
  grid-column: 1 / 3;
}
.button{
  background-color: #f2f2f2;
  border:1px solid #999;
}
.operator{
  background-color: orange;
  color: #fff;

}
</style>