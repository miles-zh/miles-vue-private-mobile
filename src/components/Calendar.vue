<template>
  <div style="height:100%;position:relative;background-color:#000">
    
    <div id="calendar">
      <div id="daysAndMonths">
        <select id="years" v-model="year" @change="showDays(year,month,ulDom)"></select>&nbsp;年
        <select id="months" v-model="month" @change="showDays(year,month,ulDom)"></select>&nbsp;月
      </div>
      <ul>
        <li>星期日</li>
        <li>星期一</li>
        <li>星期二</li>
        <li>星期三</li>
        <li>星期四</li>
        <li>星期五</li>
        <li>星期六</li>
      </ul>
      <ul id="days"></ul>
      <div class="clearfloat"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      year: "",
      month: "",
      ulDom: ""
    };
  },
  methods: {
    createOption(value, text, select) {
      var option = document.createElement("option");
      option.value = value;
      option.text = text;
      select.appendChild(option);
    },
    showDays(year, month) {
      console.log(this.ulDom);
      this.ulDom.innerHTML = "";
      //计算出这个月1号是星期几，ul中追加几个空的li
      var date = new Date(year, month - 1, 1);
      var emptyLis = date.getDay(); //获得1号是星期几
      console.log(emptyLis);
      for (var i = 0; i < emptyLis; i++) {
        this.createLi("", this.ulDom);
      }
      let dateNow = new Date(year, month, 0);
      var days = dateNow.getDate();
      for (var day = 1; day <= days; day++) {
        this.createLi(day, this.ulDom);
      }
    },
    createLi(text, parent) {
      var li = document.createElement("li");

      li.style.width = "14%";
      li.style.height = "0.8rem";
      li.style.float = "left";
      li.style.lineHeight = "0.8rem";
      li.style.backgroundColor = "#f40";
      li.style.borderRadius = "10px";
      li.style.marginLeft = "0.005rem";
      li.style.marginTop = "5px";
      li.style.color = "#fff";
      li.style.transform = "scale(0.6)";
      li.style.boxSizing = "border-box";

      li.style.fontSize = "0.5rem";
      if (text == "") {
        li.style.backgroundColor = "#000";
      }
      if (text == new Date().getDate()) {
        li.style.backgroundColor = "#04f";
        li.style.boxShadow = "1px 1px 10px #04f";
      }

      li.innerHTML = text;
      parent.appendChild(li);
    },
    initDate() {
      var now = new Date();
      var currentYear = now.getFullYear();
      var currentMonth = now.getMonth() + 1;
      this.year = currentYear;
      this.month = currentMonth;
      this.showDays(this.year, this.month);
    }
  },
  mounted() {
    let yearsDom = document.getElementById("years");
    console.log(yearsDom);
    let monthsDom = document.getElementById("months");
    this.ulDom = document.getElementById("days");

    for (var year = 1900; year < 9999; year++) {
      this.createOption(year, year, yearsDom);
    }
    for (var month = 1; month < 13; month++) {
      this.createOption(month, month, monthsDom);
    }

    //把年和月初始化为当前时间
    this.initDate();

    //创建一个li 并把这个li追加到指定的父容器
  }
};
</script>

<style scoped>
* {
  padding: 0px;
  margin: 0px;
  list-style: none;
  box-sizing: border-box;
}
#calendar {
  /*   height:440px; */

  width: 10rem;
  background-color: #000;
  text-align: center;
  position:absolute;
  height: 7rem;
  left: 50%;
  top:50%;
  transform: translateX(-50%) translateY(-50%);
}
#calendar #daysAndMonths {
  height: 1rem;
  line-height: 1rem;
  color: #fff;
  /* font-weight: bold; */
  font-size: 0.5rem;
  font-family: "微软雅黑 ";
  margin-top:0.5rem;
}
#calendar #daysAndMonths #years {
  height: 0.8rem;
  width: 1.9rem;
  border-radius: 20px;
  text-align: center;
  padding-left: 10px;
  outline: none;
  background: #f40 !important;
  color: #fff;
  font-size: 0.5rem;
}
#calendar #daysAndMonths #months {
  height: 0.8rem;
  width: 1.3rem;
  border-radius: 20px;
  text-align: center;
  padding-left: 10px;
  outline: none;
  background: #f40 !important;
  font-size: 0.5rem;
  color: #fff;
}
#calendar ul {
  width: 100%;
  margin: 0 auto;
  margin-left: 10px;
  display:flex;
  flex-wrap: wrap;
}

#calendar ul li {
  width: 14%;

  height: 0.8rem;
  line-height: 0.8rem;
  background-color: #f40;
  border-radius: 10px;
  margin-left: 0.005rem;
  margin-top: 2px;
  color: #fff;
  font-size: 0.4rem;
  transform: scale(0.6);
  box-shadow: 1px 1px 1px #f40;
}
.clearfloat {
  clear: both;
}
</style>