<template>
  <div style="height:100%">
    <div class="slider">
      <ul>
        <li>
          <a href="#bg1">雪山</a>
        </li>
        <li>
          <a href="#bg2">夕阳</a>
        </li>
        <li>
          <a href="#bg3">田野</a>
        </li>
        <li>
          <a href="#bg4">小狗</a>
        </li>
        <li>
          <a href="#bg5">荷花</a>
        </li>
      </ul>
      <img src="../assets/images/human.jpg" id="bg1"
      />
      <img src="../assets/images/cattle.jpg" id="bg2"
      />
      <img src="../assets/images/dog.jpg" id="bg3"
      />
      <img src="../assets/images/cat.jpg" id="bg4"
      />
      <img src="../assets/images/flower.jpg" id="bg5"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>

.slider {
  height: 100%;
  
  text-align: center;
  position: relative;
  width: 100%;
}
.slider ul {
  position: absolute;
  bottom: 10px;
  z-index: 999;
  width: 100%;
  
}
.slider ul li {
  display: inline-block;
  width: 1.5rem;
  
  padding-bottom: 20px;
  background-color: #02646e;
  position: relative;
  margin: 0 10px;
  height: 2rem;
  line-height: 2rem;
}
.slider ul li a {
  color: #fff;
  text-decoration: none;
  font-size: 0.5rem;
}
.slider li a::before {
  content: "";
  display: inline-block;
  width: 1rem;
  height: 1rem;
  border-radius: 50%;
  border: 2px solid #fff;
  position: absolute;
  left: 50%;
  top: -0.5rem;
  transform: translateX(-50%);
}
.slider li:nth-of-type(1) a::before {
  background: url("../assets/images/human.jpg") center;
  background-size: cover;
}
.slider li:nth-of-type(2) a::before {
  background: url("../assets/images/cattle.jpg") center;
  background-size: cover;
}
.slider li:nth-of-type(3) a::before {
  background: url("../assets/images/dog.jpg") center;
  background-size: cover;
}
.slider li:nth-of-type(4) a::before {
  background: url("../assets/images/cat.jpg") center;
  background-size: cover;
}
.slider li:nth-of-type(5) a::before {
  background: url("../assets/images/flower.jpg") center;
  background-size: cover;
}
.slider img {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
}
.slider img:nth-of-type(1) {
  z-index: 1;
}
.slider img:nth-of-type(1):target {
  z-index: 100;
  animation: sliderLeftMove 1s linear;
}
.slider img:nth-of-type(2):target {
  z-index: 100;
  /* animation: sliderLeftMove 1s linear; */
  animation: sliderBottomMove 1s linear;
}
.slider img:nth-of-type(3):target {
  z-index: 100;
  animation: zoomInMove 1s linear;
}
.slider img:nth-of-type(4):target {
  z-index: 100;
  animation: zoomOutMove 1s linear;
}
.slider img:nth-of-type(5):target {
  z-index: 100;
  animation: rotate 1s linear;
}
@keyframes sliderLeftMove {
  0% {
    left: -50%;
  }
  100% {
    left: 0;
  }
}
@keyframes sliderBottomMove {
  0% {
    top: -320px;
  }
  100% {
    top: 0px;
  }
}
@keyframes zoomInMove {
  0% {
    transform: scale(0.1);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes zoomOutMove {
  0% {
    transform: scale(2);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes rotate {
  0% {
    transform: rotate(-360deg);
  }
  100% {
    transform: rotate(0);
  }
}
</style>