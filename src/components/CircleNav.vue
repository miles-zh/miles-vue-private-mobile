<template>
  <div style="background:#555;height:100%;position:relative">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="navbar">
            请将点击此处
            <ul class="menu">
              <li>
                <a href="https://blog.csdn.net/weixin_44876003" target="_blank" title="进入我的CSDN">
                  CSDN
                </a>
                
              </li>
              <li>
                <a href="https://github.com/miles-zh" target="_blank" title="进入我的GitHub">
                GitHub
                </a>
                
              </li>
              <li>
                <a href="https://blog.csdn.net/weixin_44876003" target="_blank" title="进入我的CSDN">
                  CSDN
                </a>
                
              </li>
              <li>
                <a href="https://github.com/miles-zh" target="_blank" title="进入我的GitHub">
                GitHub
                </a>
                
              </li>
              <li>
                <a href="https://blog.csdn.net/weixin_44876003" target="_blank" title="进入我的CSDN">
                  CSDN
                </a>
                
              </li>
              <li>
                <a href="https://github.com/miles-zh" target="_blank" title="进入我的GitHub">
                GitHub
                </a>
                
              </li>
              <li>
                <a href="https://blog.csdn.net/weixin_44876003" target="_blank" title="进入我的CSDN">
                  CSDN
                </a>
                
              </li>
              <li>
                <a href="https://github.com/miles-zh" target="_blank" title="进入我的GitHub">
                GitHub
                </a>
                
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
a{
  text-decoration: none;
}
.container {
  position: absolute;
  left: 50%;
  top:53%;
  transform: translateX(-50%) translateY(-50%);
}
.container > .row {
  width: 100%;
  margin: 0 auto;
  /* height: 300px; */
}
.container > .row > .col-md-12 {
  margin-top: 75px;
}
.navbar {
  width: 5rem;
  height: 5rem;
  line-height: 5rem;
  border-radius: 50%;
  background-color: #fff;
  margin: 100px auto;
  position: relative;
  text-align: center;
  font-size: 0.5rem;
  font-weight: bold;
  color: #99b977;
  border:1px solid #99b977; 
  box-shadow: 1px 1px 20px #99b977;
}
.container > .row:hover .navbar {
  background-color: rgba(255, 255, 255, 0.8);
  transition: 0.24s 0.2s;
}
.container > .row:hover .menu {
  background-color: rgba(255, 255, 255, 0);
  transition: 0.24s 0.2s;
  cursor: pointer;
}
.menu {
  list-style: none;
  
  border-radius: 50%;
  position: absolute;
  top: 0;
  left: 0;
  height: 5rem;
  width: 5rem;  
  /* border:1px solid #000; */
  
}
.menu > li {
  position: absolute;
  top: -1.5rem;
  left: 1.75rem;
  /* border:1px solid #000;   */
  /* margin-left: 0.75rem; */
  /* margin-top: calc(130 / 30 rem); */
  transition: all 0.5s 0.1s;
  transform-origin:0.7rem 4rem  ;
  text-align: center;
  opacity: 0;
  cursor: pointer;
  height: 1.5rem;
  width: 1.5rem;
  
}
.menu > li:nth-child(1) {
  z-index: 8;
}
.menu > li:nth-child(2) {
  z-index: 7;
}
.menu > li:nth-child(3) {
  z-index: 6;
}
.menu > li:nth-child(4) {
  z-index: 5;
}
.menu > li:nth-child(5) {
  z-index: 4;
}
.menu > li:nth-child(6) {
  z-index: 3;
}
.menu > li:nth-child(7) {
  z-index: 2;
}
.menu > li > a {
  display: block;
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 50%;
  background-color: #fff;
  /*   position:absolute; */
  font-size: 60%;
  color: #99b977;
  transition: 0.6s;
  line-height: 1.5rem;
  border:1px solid #99b977;
  box-shadow: 1px 1px 20px #99b977;
}
.container > .row:hover .menu {
  transition: transform 0.4s 0.08s, z-index 0s 0.5s;

  transform: scale(0.9);
}
.container > .row:hover .menu > li {
  transition: all 0.6s;
  opacity: 1;
  cursor: pointer;
}
.container > .row:hover .menu > li:nth-child(1) {
  /*   设置延迟时间 */
  transition-delay: 0.04s;
  transform: rotate(315deg);
}
.container > .row:hover .menu > li:nth-child(1) > a {
  /*   设置延迟时间 */
  transition-delay: 0.04s;
  transform: rotate(-315deg);
}
.container > .row:hover .menu > li:nth-child(2) {
  /*   设置延迟时间 */
  transition-delay: 0.04s;
  transform: rotate(270deg);
}
.container > .row:hover .menu > li:nth-child(2) > a {
  /*   设置延迟时间 */
  transition-delay: 0.08s;
  transform: rotate(-270deg);
}
.container > .row:hover .menu > li:nth-child(3) {
  /*   设置延迟时间 */
  transition-delay: 0.1s;
  transform: rotate(225deg);
}
.container > .row:hover .menu > li:nth-child(3) > a {
  /*   设置延迟时间 */
  transition-delay: 0.1s;
  transform: rotate(-225deg);
}
.container > .row:hover .menu > li:nth-child(4) {
  /*   设置延迟时间 */
  transition-delay: 0.12s;
  transform: rotate(180deg);
}
.container > .row:hover .menu > li:nth-child(4) > a {
  /*   设置延迟时间 */
  transition-delay: 0.12s;
  transform: rotate(-180deg);
}
.container > .row:hover .menu > li:nth-child(5) {
  /*   设置延迟时间 */
  transition-delay: 0.14s;
  transform: rotate(135deg);
}
.container > .row:hover .menu > li:nth-child(5) > a {
  /*   设置延迟时间 */
  transition-delay: 0.14s;
  transform: rotate(-135deg);
}
.container > .row:hover .menu > li:nth-child(6) {
  /*   设置延迟时间 */
  transition-delay: 0.16s;
  transform: rotate(90deg);
}
.container > .row:hover .menu > li:nth-child(6) > a {
  /*   设置延迟时间 */
  transition-delay: 0.16s;
  transform: rotate(-90deg);
}
.container > .row:hover .menu > li:nth-child(7) {
  /*   设置延迟时间 */
  transition-delay: 0.18s;
  transform: rotate(45deg);
}
.container > .row:hover .menu > li:nth-child(7) > a {
  /*   设置延迟时间 */
  transition-delay: 0.18s;
  transform: rotate(-45deg);
}
</style>