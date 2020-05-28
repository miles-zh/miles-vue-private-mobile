<template>
  <div style="height:100%;margin:0">
    <div class="wrapper" ref="wrapper">
      <ul ref="ul">
        <li>
          <img src="../assets/images/human.jpg" alt />
        </li>
        <li>
          <img src="../assets/images/cat.jpg" alt />
        </li>

        <li>
          <img src="../assets/images/cattle.jpg" alt />
        </li>
        <li>
          <img src="../assets/images/dog.jpg" alt />
        </li>
      </ul>
      <div class="btn" ref="btns">
        <a href="#" class="btnleft" @touchstart="moveLeft">&lt;</a>
        <a href="#" class="btnright" @touchstart="moveRight">&gt;</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      config: [
        {
          width: 5,
          height: 3,
          top: 0,
          left: 0,
          opacity: 1,
          zIndex: 1
        },
        {
          width: 4,
          height: 2.2,
          top: -1,
          left: -2,
          opacity: 0.8,
          zIndex: -1
        },
        {
          width: 3.6,
          height: 1.9,
          top: -2,
          left: 1,
          opacity: 0.5,
          zIndex: -2
        },
        {
          width: 4,
          height: 2.2,
          top: -1,
          left: 3,
          opacity: 0.8,
          zIndex: -1
        }
      ],
      leader: null,
      target: null,
      step: null,
      flag: true,
      timer: null,
      flag1: true,
      btnOpacity: 0,
      ul: null,
      lis: null,
      btn: null,
      wrap: null
    };
  },

  mounted() {
    this.lis = this.$refs.ul.children;
    for (var i = 0; i < this.lis.length; i++) {
      this.animate(this.lis[i], this.config[i]);
    }

    let _this = this;
    setTimeout(() => {
      _this.autoPlay();
    }, 3000);
  },
  created() {},
  methods: {
    animate(obj, json, fn1) {
      clearInterval(obj.timer);
      obj.timer = setInterval(function() {
        let flag = true;
        // console.log('a');
        for (var key in json) {
          if (key === "opacity") {
            // console.log("b")
            this.leader = window.getComputedStyle(obj)[key] * 100;
            // console.log(leader)
            this.target = json[key] * 100;
            this.step = (this.target - this.leader) / 10;
            this.step =
              this.step > 0 ? Math.ceil(this.step) : Math.floor(this.step);
            this.leader = this.leader + this.step;
            // console.log(leader+"A")
            obj.style[key] = this.leader / 100;
          } else if (key === "zIndex") {
            obj.style[key] = json.zIndex;
          } else {
            this.leader = parseInt(window.getComputedStyle(obj)[key]);
            // console.log(window.getComputedStyle(obj)[key])
            this.target =
              (parseInt(json[key]) * document.documentElement.clientWidth) / 10;
            this.step = (this.target - this.leader) / 10;
            this.step =
              this.step > 0 ? Math.ceil(this.step) : Math.floor(this.step);

            this.leader = this.leader + this.step;

            obj.style[key] = this.leader + "px";
          }
          // console.log(target)
          if (this.target != this.leader) {
            flag = false;
          }
        }
        if (flag) {
          clearInterval(obj.timer);
          if (fn1) {
            fn1();
          }
        }
        // console.log("animate")
      }, 15);
    },
    moveLeft() {
      // console.log(this.lis)
      // console.log("a")
      // console.log(this.flag1)
      clearInterval(this.timer);
      this.timer=null
      // console.log(this.flag1)
      if (this.flag1) {
        this.flag1 = false;
        this.config.push(this.config.shift());
        for (var i = 0; i < this.lis.length; i++) {
          this.animate(this.lis[i], this.config[i], function() {});
        }
        this.flag1 = true;
      }
      setTimeout(()=>{
        this.autoPlay()
      },5000)
    },
    moveRight() {
      clearInterval(this.timer)
      this.timer=null
      let _this = this;
      if (_this.flag1) {
        _this.flag1 = false;
        _this.config.unshift(_this.config.pop());
        for (var i = 0; i < _this.lis.length; i++) {
          _this.animate(_this.lis[i], _this.config[i], function() {});
        }
        _this.flag1 = true;
      }
      setTimeout(()=>{
        this.autoPlay()
      },5000)
    },
    autoPlay() {
      let _this = this;
      _this.timer = setInterval(() => {
      if (_this.flag1) {
        _this.flag1 = false;
        _this.config.unshift(_this.config.pop());
        for (var i = 0; i < _this.lis.length; i++) {
          _this.animate(_this.lis[i], _this.config[i], function() {});
        }
        _this.flag1 = true;
      }
      }, 3000);
    }
  }
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
a {
  text-decoration: none;
  color: #fff;
  font-weight: bold;
  background-color: rgba(0, 0, 0, 0.5);
}
.wrapper {
  position: relative;
  width: 100%;
  margin: 3rem auto;
}
ul {
  list-style: none;
  position: relative;
  width: 5rem;
  height: 3rem;
  margin: 0 auto;
}
ul li {
  position: absolute;
  height: 100%;
  width: 100%;
  /*   z-index:0; */
}
.btn {
  font-size: 1rem;
  width: 5rem;
  z-index: 999;
  position: absolute;
  height: 1rem;
  line-height: 1rem;
  background-color: rgba(0, 0, 0, 0);
  text-align: center;
  top: 130%;
  left: 50%;
  transform: translateX(-50%);
  opacity: 1;
}
img {
  width: 100%;
  height: 100%;
}
.btnleft {
  float: left;
  padding:0 0.91rem;
  background-color: rgb(29, 26, 26);
}
.btnright {
  float: right;
  padding:0 0.91rem;
  background-color: rgb(29, 26, 26);
}
</style>