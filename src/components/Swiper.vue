<template>
  <div>
    <div id="wrap">
      <div id="pic" ref="pic">
        <ul ref="ul"></ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  created() {},
  methods: {
    lunbo(ul) {
      let k = 0;
      setInterval(function() {
        for (let j = 0; j < ul.children.length; j++) {
          ul.children[j].style.transform = `rotateX(${-90 * (k + 1)}deg)`;

          ul.children[j].style.transition = "1s";
          ul.children[j].style.transitionDelay = `${j * 0.1}s`;
        }
        k++;
        if (k > 4) {
          k = 0;
          for (let j = 0; j < ul.children.length; j++) {
            ul.children[j].style.transform = `rotateX(0deg)`;
            ul.children[j].style.transition = "none";
          }
        }
      }, 1200);
    },
    play(n, ul) {
      let width = this.$refs.pic.offsetWidth / n;
      for (let i = 0; i < n; i++) {
        let li = document.createElement("li");
        li.style.height = "100%";
        li.style.width = width-1 + "px";
        li.style.float = "left";
        li.style.boxSizing = "border-box";
        li.style.position = "relative";
        li.style.transformStyle = "preserve-3d";
        li.style.transition = "1s";
        li.style.perspective = "90000px";
        for (let j = 0; j < 4; j++) {
          let div = document.createElement("div");
          div.style.width = width + "px";
          div.style.height = "100%";
          div.style.position = "absolute";
          div.style.textAlign = "center";
          div.style.lineHeight = "6rem";
          div.style.backgroundSize = "400%,100%";
          div.style.backgroundPosition = `${-1 * i * width}px 0px`;
          if (j == 0) {
            div.style.top = "-6rem";
            div.style.transformOrigin = "bottom";
            div.style.transform = "translateZ(3rem) rotateX(90deg)";
            div.style.backgroundImage = "url(https://s1.ax1x.com/2020/05/24/tScHNn.jpg)";
          }
          if (j == 1) {
            div.style.top = "6rem";
            div.style.transformOrigin = "top";
            div.style.transform = "translateZ(3rem) rotateX(-90deg)";
            div.style.backgroundImage = "url(https://s1.ax1x.com/2020/05/24/tSgCNR.jpg)";
          }
          if (j == 2) {
            div.style.transform = "translateZ(3rem)";
            div.style.backgroundImage = "url(https://s1.ax1x.com/2020/05/24/tSglCt.jpg)";
          }
          if (j == 3) {
            div.style.transform = "translateZ(-3rem) rotateX(180deg)";
            div.style.backgroundImage = "url(https://s1.ax1x.com/2020/05/24/tSgd5n.jpg)";
          }
          li.appendChild(div);
        }
        ul.appendChild(li);
      }
    }
  },
  mounted() {
    this.play(4, this.$refs.ul);
    this.lunbo(this.$refs.ul);
  }
};
</script>

<style scoped>
ul {
  list-style: none;
}
#wrap {
  width: 90%;
  height: 6rem;
  margin: 3rem auto;
  /*   border:1px solid #f40; */
  position: relative;
}
#pic {
  width: 100%;
  height: 6rem;
  /*    设置视角，景深*/
  perspective: 90000px;
}
#pic > ul {
  perspective: 90000px;
  height: 6rem;
  width: 100%;
  transform-style: preserve-3d;
  padding-left: 0;
}
</style>