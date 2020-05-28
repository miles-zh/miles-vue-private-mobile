<template>
  <div>
    <div id="container">
      <div id="mian">
        <div class="square one">1</div>
        <div class="square two">2</div>
        <div class="square three">3</div>
        <div class="square four">4</div>
        <div class="square five">5</div>
        <div class="square six">6</div>
      </div>
    </div>
  </div>
</template>

<script scoped>
export default {};
</script>

<style>
    #container{
  margin:4rem auto;
  width:4rem;
  perspective:28rem;
  height:4rem;
}
#mian{
  position:relative;
  width: 2rem;
  height:2rem;
  transform-style:preserve-3d;
  /* background-color: #000; */
  animation: ball 5s linear infinite;
  transform-origin:50% 50%;
  margin-left: 1rem;
}
@keyframes ball{
  0%{
    transform:rotateX(0) rotateY(0) ;
  }
  100%{
    transform:rotateX(360deg) rotateY(360deg);
  }
}
.square{
  height: 4rem;
  width: 4rem;
  border:1px solid #ccc;
  position:absolute;
  text-align:center;
  line-height:4rem;
  font-size:1rem;
  font-weight:bold;
}
.one{ 
  transform:translate3d(-2rem,0px,0px) rotateY(90deg); 
  background-color: rgba(100,200,100,0.5);
}
.two{
  transform:translate3d(2rem,0px,0px) rotateY(90deg) ;
  background-color: rgba(100,200,100,0.5);
}
.three{ 
  transform:translate3d(0px,0px,-2rem);
  background-color: rgba(100,100,200,0.5);
}
.four{
  transform:translate3d(0px,0px,2rem);
  background-color: rgba(100,100,200,0.5);
}
.five{ 
  transform:rotateX(90deg) translate3d(0px,0px,2rem); 
  background-color: rgba(200,100,100,0.5)
}
.six{
  transform:rotateX(-90deg) translate3d(0px,0px,2rem);
  background-color: rgba(200,100,100,0.5)
}
</style>