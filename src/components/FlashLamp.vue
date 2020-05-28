<template>
  <div class="flash-lamp-container">
    <div class="flash-lamp-wrap">
      <div class="top-row">
        <div class="item item01"></div>
        <div class="item item02"></div>
        <div class="item item03"></div>
        <div class="item item04"></div>
        <div class="item item05"></div>
        <div class="item item06"></div>
        <div class="item item07"></div>
        <div class="item item08"></div>
        <div class="item item09"></div>
        <div class="item item10"></div>
        <div class="item item11"></div>
        <!-- <div class="item item12"></div> -->
        
      </div>
      <div class="right-column">
        <div class="item item01"></div>
        <div class="item item02"></div>
        <div class="item item03"></div>
        <div class="item item04"></div>
        <div class="item item05"></div>
        <div class="item item06"></div>
        <div class="item item07"></div>
        <div class="item item08"></div>
        <div class="item item09"></div>
        <div class="item item10"></div>
        <div class="item item11"></div>
        <!-- <div class="item item12"></div>
        <div class="item item13"></div> -->
      </div>
      <div class="bottom-row">
        <div class="item item01"></div>
        <div class="item item02"></div>
        <div class="item item03"></div>
        <div class="item item04"></div>
        <div class="item item05"></div>
        <div class="item item06"></div>
        <div class="item item07"></div>
        <div class="item item08"></div>
        <div class="item item09"></div>
        <div class="item item10"></div>
        <div class="item item11"></div>
        <div class="item item12"></div>
        
      </div>
      <div class="left-column">
        <div class="item item01"></div>
        <div class="item item02"></div>
        <div class="item item03"></div>
        <div class="item item04"></div>
        <div class="item item05"></div>
        <div class="item item06"></div>
        <div class="item item07"></div>
        <div class="item item08"></div>
        <div class="item item09"></div>
        <div class="item item10"></div>
        <div class="item item11"></div>
        <!-- <div class="item item12"></div>
        <div class="item item13"></div> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
$color1: #030;
$color2: #360;
$color3: #690;
$color4: #060;

$color5: #390;
$color6: #6c0;
$color7: #090;

$color8: #3c0;
$color9: #0c0;

$color10: #6f0;
$color11: #3f0;


.flash-lamp-container{
    height: 100%;
    // background-color: #000;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}


.flash-lamp-wrap {
  height: 6rem;
  width: 6rem;
  
  
  position: absolute;

  .item {
    width: 0rem;
    border-bottom: 0.5rem solid #030;
    border-left: 0.5rem solid transparent;
    border-right: 0.5rem solid transparent;
  }

  .top-row {
    display: flex;
    width: 6rem;
    margin: auto;
    transform: rotateZ(180deg) rotateY(180deg);
    .item02 {
      border-bottom: 0.5rem solid $color2;
      transform: rotate(180deg) translateX(0.5rem);
    }
    .item03 {
      border-bottom: 0.5rem solid $color3;
      transform: translateX(-1rem);
    }
    .item04 {
      border-bottom: 0.5rem solid $color4;
      transform: rotate(180deg) translateX(1.5rem);
    }
    .item05 {
      border-bottom: 0.5rem solid $color5;
      transform: translateX(-2rem);
    }
    .item06 {
      border-bottom: 0.5rem solid $color6;
      transform: rotate(180deg) translateX(2.5rem);
    }
    .item07 {
      border-bottom: 0.5rem solid $color7;
      transform: translateX(-3rem);
    }
    .item08 {
      border-bottom: 0.5rem solid $color8;
      transform: rotate(180deg) translateX(3.5rem);
    }
    .item09 {
      border-bottom: 0.5rem solid $color9;
      transform: translateX(-4rem);
    }
    .item10 {
      border-bottom: 0.5rem solid $color10;
      transform: rotate(180deg) translateX(4.5rem);
    }
    .item11 {
      border-bottom: 0.5rem solid $color11;
      transform: translateX(-5rem);
    }
    // .item12 {
    //   border-bottom: 0.5rem solid $color12;
    //   transform: rotate(180deg) translateX(5.5rem);
    // }
    
  }

  .right-column {
    display: flex;
    flex-direction: column;
    width: 1rem;
    position: absolute;
    right: -.25rem;
    top: .25rem;
    .item01 {
      border-bottom: 0.5rem solid $color1;
      transform: rotate(270deg);
    }
    .item02 {
      border-bottom: 0.5rem solid $color2;
      transform: rotate(90deg);
    }
    .item03 {
      border-bottom: 0.5rem solid $color3;
      transform: rotate(270deg);
    }
    .item04 {
      border-bottom: 0.5rem solid $color4;
      transform: rotate(90deg);
    }
    .item05 {
      border-bottom: 0.5rem solid $color5;
      transform: rotate(270deg);
    }
    .item06 {
      border-bottom: 0.5rem solid $color6;
      transform: rotate(90deg);
    }
    .item07 {
      border-bottom: 0.5rem solid $color7;
      transform: rotate(270deg);
    }
    .item08 {
      border-bottom: 0.5rem solid $color8;
      transform: rotate(90deg);
    }
    .item09 {
      border-bottom: 0.5rem solid $color9;
      transform: rotate(270deg);
    }
    .item10 {
      border-bottom: 0.5rem solid $color10;
      transform: rotate(90deg);
    }
    .item11 {
      border-bottom: 0.5rem solid $color11;
      transform: rotate(270deg);
    }
    
  }
  .bottom-row {
      display: flex;
      position: absolute;
      bottom: 0rem;
      width: 6rem;
      transform: rotateZ(180deg) rotateX(180deg) ;
      left: 0rem;
      
    .item02 {
      border-bottom: 0.5rem solid $color2;
      transform: rotate(180deg) translateX(0.5rem);
    }
    .item03 {
      border-bottom: 0.5rem solid $color3;
      transform: translateX(-1rem);
    }
    .item04 {
      border-bottom: 0.5rem solid $color4;
      transform: rotate(180deg) translateX(1.5rem);
    }
    .item05 {
      border-bottom: 0.5rem solid $color5;
      transform: translateX(-2rem);
    }
    .item06 {
      border-bottom: 0.5rem solid $color6;
      transform: rotate(180deg) translateX(2.5rem);
    }
    .item07 {
      border-bottom: 0.5rem solid $color7;
      transform: translateX(-3rem);
    }
    .item08 {
      border-bottom: 0.5rem solid $color8;
      transform: rotate(180deg) translateX(3.5rem);
    }
    .item09 {
      border-bottom: 0.5rem solid $color9;
      transform: translateX(-4rem);
    }
    .item10 {
      border-bottom: 0.5rem solid $color10;
      transform: rotate(180deg) translateX(4.5rem);
    }
    .item11 {
      border-bottom: 0.5rem solid $color11;
      transform: translateX(-5rem);
    }
    // .item12 {
    //   border-bottom: 0.5rem solid $color12;
    //   transform: rotate(180deg) translateX(5.5rem);
    // }
  }
  .left-column{
      display: flex;
    flex-direction: column;
    width: 1rem;
    position: absolute;
    top: .25rem;
    left:  -.25rem;
    transform: rotateY(180deg) rotateX(180deg);
    .item01 {
      border-bottom: 0.5rem solid $color1;
      transform: rotate(270deg);
    }
    .item02 {
      border-bottom: 0.5rem solid $color2;
      transform: rotate(90deg);
    }
    .item03 {
      border-bottom: 0.5rem solid $color3;
      transform: rotate(270deg);
    }
    .item04 {
      border-bottom: 0.5rem solid $color4;
      transform: rotate(90deg);
    }
    .item05 {
      border-bottom: 0.5rem solid $color5;
      transform: rotate(270deg);
    }
    .item06 {
      border-bottom: 0.5rem solid $color6;
      transform: rotate(90deg);
    }
    .item07 {
      border-bottom: 0.5rem solid $color7;
      transform: rotate(270deg);
    }
    .item08 {
      border-bottom: 0.5rem solid $color8;
      transform: rotate(90deg);
    }
    .item09 {
      border-bottom: 0.5rem solid $color9;
      transform: rotate(270deg);
    }
    .item10 {
      border-bottom: 0.5rem solid $color10;
      transform: rotate(90deg);
    }
    .item11 {
      border-bottom: 0.5rem solid $color11;
      transform: rotate(270deg);
    }
  }
}

.item01{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation01 5s ease 0s infinite;
}
.item02{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation02 5s ease 0s infinite;
}
.item03{
   
    animation: animation03 5s ease 0s infinite;
}
.item04{
   
    animation: animation04 5s ease 0s infinite;
}
.item05{
   
    animation: animation05 5s ease 0s infinite;
}

.item06{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation06 5s ease 0s infinite;
}

.item07{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation07 5s ease 0s infinite;
}
.item08{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation08 5s ease 0s infinite;
}
.item09{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation09 5s ease 0s infinite;
}
.item10{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation10 5s ease 0s infinite;
}
.item11{
    // animation: name duration timing-function delay iteration-count direction fill-mode;
    animation: animation11 5s ease 0s infinite;
}



@keyframes animation01 {

    0%{
        border-bottom: 0.5rem solid $color1;
    }

    10%{
        border-bottom: 0.5rem solid $color2;
    }
    20%{
        border-bottom: 0.5rem solid $color3;
    }
    30%{
        border-bottom: 0.5rem solid $color4;
    }
    40%{
        border-bottom: 0.5rem solid $color5;
    }
    50%{
        border-bottom: 0.5rem solid $color6;
    }
    60%{
        border-bottom: 0.5rem solid $color7;
    }
    70%{
        border-bottom: 0.5rem solid $color8;
    }
    80%{
        border-bottom: 0.5rem solid $color9;
    }
    90%{
        border-bottom: 0.5rem solid $color10;
    }
    100%{
        border-bottom: 0.5rem solid $color11;
    }
}

@keyframes animation02 {

    0%{
        border-bottom: 0.5rem solid $color2;
    }

    10%{
        border-bottom: 0.5rem solid $color3;
    }
    20%{
        border-bottom: 0.5rem solid $color4;
    }
    30%{
        border-bottom: 0.5rem solid $color5;
    }
    40%{
        border-bottom: 0.5rem solid $color6;
    }
    50%{
        border-bottom: 0.5rem solid $color7;
    }
    60%{
        border-bottom: 0.5rem solid $color8;
    }
    70%{
        border-bottom: 0.5rem solid $color9;
    }
    80%{
        border-bottom: 0.5rem solid $color10;
    }
    90%{
        border-bottom: 0.5rem solid $color11;
    }
    100%{
        border-bottom: 0.5rem solid $color1;
    }
}

@keyframes animation03 {

    0%{
        border-bottom: 0.5rem solid $color3;
    }

    10%{
        border-bottom: 0.5rem solid $color4;
    }
    20%{
        border-bottom: 0.5rem solid $color5;
    }
    30%{
        border-bottom: 0.5rem solid $color6;
    }
    40%{
        border-bottom: 0.5rem solid $color7;
    }
    50%{
        border-bottom: 0.5rem solid $color8;
    }
    60%{
        border-bottom: 0.5rem solid $color9;
    }
    70%{
        border-bottom: 0.5rem solid $color10;
    }
    80%{
        border-bottom: 0.5rem solid $color11;
    }
    90%{
        border-bottom: 0.5rem solid $color1;
    }
    100%{
        border-bottom: 0.5rem solid $color2;
    }
}
@keyframes animation04 {

    0%{
        border-bottom: 0.5rem solid $color4;
    }

    10%{
        border-bottom: 0.5rem solid $color5;
    }
    20%{
        border-bottom: 0.5rem solid $color6;
    }
    30%{
        border-bottom: 0.5rem solid $color7;
    }
    40%{
        border-bottom: 0.5rem solid $color8;
    }
    50%{
        border-bottom: 0.5rem solid $color9;
    }
    60%{
        border-bottom: 0.5rem solid $color10;
    }
    70%{
        border-bottom: 0.5rem solid $color11;
    }
    80%{
        border-bottom: 0.5rem solid $color1;
    }
    90%{
        border-bottom: 0.5rem solid $color2;
    }
    100%{
        border-bottom: 0.5rem solid $color3;
    }
}


@keyframes animation05 {

    0%{
        border-bottom: 0.5rem solid $color5;
    }

    10%{
        border-bottom: 0.5rem solid $color6;
    }
    20%{
        border-bottom: 0.5rem solid $color7;
    }
    30%{
        border-bottom: 0.5rem solid $color8;
    }
    40%{
        border-bottom: 0.5rem solid $color9;
    }
    50%{
        border-bottom: 0.5rem solid $color10;
    }
    60%{
        border-bottom: 0.5rem solid $color11;
    }
    70%{
        border-bottom: 0.5rem solid $color1;
    }
    80%{
        border-bottom: 0.5rem solid $color2;
    }
    90%{
        border-bottom: 0.5rem solid $color3;
    }
    100%{
        border-bottom: 0.5rem solid $color4;
    }
}

@keyframes animation06 {

    0%{
        border-bottom: 0.5rem solid $color6;
    }

    10%{
        border-bottom: 0.5rem solid $color7;
    }
    20%{
        border-bottom: 0.5rem solid $color8;
    }
    30%{
        border-bottom: 0.5rem solid $color9;
    }
    40%{
        border-bottom: 0.5rem solid $color10;
    }
    50%{
        border-bottom: 0.5rem solid $color11;
    }
    60%{
        border-bottom: 0.5rem solid $color1;
    }
    70%{
        border-bottom: 0.5rem solid $color2;
    }
    80%{
        border-bottom: 0.5rem solid $color3;
    }
    90%{
        border-bottom: 0.5rem solid $color4;
    }
    100%{
        border-bottom: 0.5rem solid $color5;
    }
}

@keyframes animation07 {

    0%{
        border-bottom: 0.5rem solid $color7;
    }

    10%{
        border-bottom: 0.5rem solid $color8;
    }
    20%{
        border-bottom: 0.5rem solid $color9;
    }
    30%{
        border-bottom: 0.5rem solid $color10;
    }
    40%{
        border-bottom: 0.5rem solid $color11;
    }
    50%{
        border-bottom: 0.5rem solid $color1;
    }
    60%{
        border-bottom: 0.5rem solid $color2;
    }
    70%{
        border-bottom: 0.5rem solid $color3;
    }
    80%{
        border-bottom: 0.5rem solid $color4;
    }
    90%{
        border-bottom: 0.5rem solid $color5;
    }
    100%{
        border-bottom: 0.5rem solid $color6;
    }
}
@keyframes animation08 {

    0%{
        border-bottom: 0.5rem solid $color8;
    }

    10%{
        border-bottom: 0.5rem solid $color9;
    }
    20%{
        border-bottom: 0.5rem solid $color10;
    }
    30%{
        border-bottom: 0.5rem solid $color11;
    }
    40%{
        border-bottom: 0.5rem solid $color1;
    }
    50%{
        border-bottom: 0.5rem solid $color2;
    }
    60%{
        border-bottom: 0.5rem solid $color3;
    }
    70%{
        border-bottom: 0.5rem solid $color4;
    }
    80%{
        border-bottom: 0.5rem solid $color5;
    }
    90%{
        border-bottom: 0.5rem solid $color6;
    }
    100%{
        border-bottom: 0.5rem solid $color7;
    }
}

@keyframes animation09 {

    0%{
        border-bottom: 0.5rem solid $color9;
    }

    10%{
        border-bottom: 0.5rem solid $color10;
    }
    20%{
        border-bottom: 0.5rem solid $color11;
    }
    30%{
        border-bottom: 0.5rem solid $color1;
    }
    40%{
        border-bottom: 0.5rem solid $color2;
    }
    50%{
        border-bottom: 0.5rem solid $color3;
    }
    60%{
        border-bottom: 0.5rem solid $color4;
    }
    70%{
        border-bottom: 0.5rem solid $color5;
    }
    80%{
        border-bottom: 0.5rem solid $color6;
    }
    90%{
        border-bottom: 0.5rem solid $color7;
    }
    100%{
        border-bottom: 0.5rem solid $color8;
    }
}

@keyframes animation10 {

    0%{
        border-bottom: 0.5rem solid $color10;
    }

    10%{
        border-bottom: 0.5rem solid $color11;
    }
    20%{
        border-bottom: 0.5rem solid $color1;
    }
    30%{
        border-bottom: 0.5rem solid $color2;
    }
    40%{
        border-bottom: 0.5rem solid $color3;
    }
    50%{
        border-bottom: 0.5rem solid $color4;
    }
    60%{
        border-bottom: 0.5rem solid $color5;
    }
    70%{
        border-bottom: 0.5rem solid $color6;
    }
    80%{
        border-bottom: 0.5rem solid $color7;
    }
    90%{
        border-bottom: 0.5rem solid $color8;
    }
    100%{
        border-bottom: 0.5rem solid $color9;
    }
}

@keyframes animation11 {

    0%{
        border-bottom: 0.5rem solid $color11;
    }

    10%{
        border-bottom: 0.5rem solid $color1;
    }
    20%{
        border-bottom: 0.5rem solid $color2;
    }
    30%{
        border-bottom: 0.5rem solid $color3;
    }
    40%{
        border-bottom: 0.5rem solid $color4;
    }
    50%{
        border-bottom: 0.5rem solid $color5;
    }
    60%{
        border-bottom: 0.5rem solid $color6;
    }
    70%{
        border-bottom: 0.5rem solid $color7;
    }
    80%{
        border-bottom: 0.5rem solid $color8;
    }
    90%{
        border-bottom: 0.5rem solid $color9;
    }
    100%{
        border-bottom: 0.5rem solid $color10;
    }
}














</style>