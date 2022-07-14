<template>
  <body id="popup">
    <div id="center">
      <div class="welcome"></div>
      <div class="triangle"></div>
      <div class="little_triangle"></div>
      <div class="mainInfo"></div>
      <div id="info">
        <h2 class="user_name" id="username">Tracy</h2>
        <div class="info_main">
          <div class="label_text">
            <p>已连接</p>   
            <p>Duration</p> 
          </div>
          <div class="text">
          <span id="clock">18:15:59</span>
          <span class="unit"></span>
          </div>
          <div class="label_text">
            <p>已用流量</p>
            <p>Usage</p> 
          </div>
          <div class="usage_bar">
            <ul class="calibration">
              <li>125</li>
              <li>100</li>
              <li>75</li>
              <li>50</li>
            </ul>
            <div id="usage_value"></div>
            <div class="stripe"></div>
            <div class="stripe second_stripe"></div>
            <div class="text">
              <span class="unit" id="usage_flux">25G</span>
            </div>
          </div>
        </div>
      </div>
      <div class="bar">
        <button class="disconnect"></button>
      </div>
      <ui id="links">
        <li>
          <a id="link_info" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421f9f9479369247b59700f81b9991b2631506205de" 
          target="_new" title="清华信息门户info.tsinghua">Info</a>
        </li>
        <li>
          <a id="link_lib" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fcfe43d23323615e79009cadd6502720703f47/" 
          target="_new" title="清华图书馆lib.tsinghua">Lib</a>
        </li>
        <li>
          <a id="link_learn" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fcf2408e297e7c4377068ea48d546d30ca8cc97bcc/" 
          target="_new" title="清华网络学堂learn.tsinghua">Learn</a>
        </li>
        <li>
          <a id="link_mail" href="https://webvpn.tsinghua.edu.cn/http/77726476706e69737468656265737421fdf6489069247b59700f81b9991b263165e79cae/" 
          target="_new" title="清华邮箱mail.tsinghua">Mail</a>
        </li>
      </ui>
    </div>
  </body>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

// export default {
//   name: 'App',
//   components: {
//     HelloWorld
//   }
// }
</script>

<style>
* {
    margin: 0;
    padding: 0;
    border: 0;
}
body {
    background: #E6E6E6  repeat-x top;
    min-width: 768px;
    font-family: "Microsoft YaHei", "SimHei", "Apple LiGothic Medium";
}

.welcome{
    text-indent: -999em;
    overflow: hidden;
}
#popup {
    min-width: 640px;
    min-height: 480px;
    background: #E6E6E6 url(~@/assets/bg.png) no-repeat top right;
    
}
#popup #center {
    position: relative;
    width: 640px;
    height: 480px;
    background: url(~@/assets/shadow.png) no-repeat 48px 344px;
}
#center {
    margin: auto;
    width: 768px;
    height: 100%;
}
.welcome {
    position: absolute;
    box-shadow: 0 0 8px rgb(0 0 0 / 10%);
}
#popup .welcome {
    top: 64px;
    left: 48px;
    width: 512px;
    height: 224px;
    background: #E64E2E url(~@/assets/greeting.png) no-repeat 30px 46px;
}
#popup .triangle {
    left: 80px;
    top: 288px;
}
.triangle {
    position: absolute;
    border-color: #E64E2E transparent;
    border-width: 48px 48px 0 0;
}
.triangle {
    position: absolute;
    top: 304px;
    left: 32px;
    border-color: #E64E2E transparent;
    border-width: 48px 48px 0 0;
}
#popup .little_triangle {
    position: absolute;
    top: 288px;
    left: 592px;
    border-color: transparent #CCCCCC;
    border-width: 16px 0 0 16px;
}
.little_triangle, .triangle{
    width: 0;
    height: 0;
    border-style: solid;
}
/*  */
#popup #info {
    top: 96px;
    left: 176px;
    padding: 32px;
    width: 352px;
    height: 208px;
}
#login, #popup #info {
    position: absolute;
    background: #F2F2F2;
    box-shadow: 0 0 8px rgb(0 0 0 / 10%);
}
#info .user_name {
    float: left;
    color: #E64E2E;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 34px;
    font-weight: lighter;
}

#info .label_text {
    clear: left;
    float: left;
    width: 56px;
    height: 32px;
    margin-top: 22px;
    text-align: right;
    font-size: 13px;
}
#info .text {
    float: left;
    margin: 24px 0 0 20px;
    padding-top: 4px;
    height: 28px;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 24px;
    font-weight: lighter;
}
#clock {
    color: #ec6677;
}
#info .text .unit {
    margin-left: 8px;
    color: #5C5C5C;
}
#popup .bar {
    position: absolute;
    top: 304px;
    right: 32px;
    width: 208px;
    height: 80px;
    background: #FFFFFF;
    box-shadow: 0 0 8px rgb(0 0 0 / 10%);
}
.disconnect {
    margin: 16px;
    width: 174px;
    height: 46px;
    border: #B2AABE solid 1px;
    background: #C0BDCC url(~@/assets/disconnect.png) no-repeat center 0;
    overflow: hidden;
}
#info .usage_bar {
    position: relative;
    float: left;
    margin: 24px 0 0 16px;
    padding: 0;
    width: 280px;
    height: 32px;
    background: url(~@/assets/usage_bg.gif) repeat-y;
}
.usage_bar .calibration {
    position: absolute;
    top: -30px;
    right: 14px;
    font-family: Verdana, Geneva, sans-serif;
    font-size: 13px;
    color: #969696;
}
ul {
    list-style: none;
}
.calibration li {
    float: right;
    width: 53px;
    text-align: right;
}
.usage_bar #usage_value {
    width: 55px;
    float: left;
    height: 32px;
    max-width: 280px;
    background: #FBB03B;
}
.usage_bar .stripe {
    position: absolute;
    top: 0;
    right: 4px;
    width: 4px;
    height: 100%;
    background: #F2F2F2;
}
.usage_bar .second_stripe {
    right: 12px;
}
#info .usage_bar .text {
    position: absolute;
    top: 2px;
    left: 4px;
    float: none;
    margin: 0;
    padding: 0;
}
info .text .unit {
    margin-left: 8px;
    color: #5C5C5C;
    font-size: 24px;
}
/*  */
#popup #links {
    position: absolute;
    list-style: none;
    bottom: 32px;
    right: 32px;
    width: 234px;
}
ul {
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-inline-start: 40px;
}
#links li {
    float: left;
    margin-right: 7px;
    font-size: 11px;
    font-family: Verdana, Geneva, sans-serif;
}
li {
    display: list-item;
    text-align: -webkit-match-parent;
}
#links li a {
    display: block;
    padding: 16px 0 0 26px;
    height: 16px;
}
a {
    color: #AD3B23;
    text-decoration: none;
}
a:-webkit-any-link {
    cursor: pointer;
}
#links #link_info {
    background: url(~@/assets/info.gif) no-repeat 2px 2px;
}
#links #link_lib {
    background: url(~@/assets/lib.gif) no-repeat 2px 2px;
}
#links #link_learn {
    background: url(~@/assets/learn.gif) no-repeat 4px 1px;
}
#links #link_mail {
    background: url(~@/assets/mail.gif) no-repeat 0 1px;
}
</style>
