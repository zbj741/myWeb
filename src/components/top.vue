<template>
  <div class="top">
    <div class="container">
      <slot></slot>
      <div class="banner">
        <div class="avator"><img
            src="../common/images/avator.jpg"
            alt=""
          ></div>
        <div class="info">
          <h5 class="hello">您好</h5>
          <h1>{{info.name}}</h1>
          <h6 class="text_hidden">{{info.job}}</h6>
          <ul>
            <li class="text_hidden"><b>出生年月</b> <span>{{info.birth}}</span></li>
            <li class="text_hidden"><b>电子邮箱</b> <span>{{info.email}}</span></li>
            <li class="text_hidden"><b>手机号码</b> <span>{{info.phone}}</span></li>
            <li class="text_hidden"><b>本科院校</b> <span>{{info.undergraduate}}</span></li>
            <li class="text_hidden"><b>研究生院校</b> <span>{{info.postgraduate}}</span></li>
          </ul>
        </div>
        <div class="clearfix"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "top",
  data() {
    return {
      info: {
        name: "我是张伯钧",
        job: "北京航空航天大学在读研究生",
        birth: "1997-02-16",
        email: "zbj5001@126.com",
        phone: "15810272093",
        undergraduate: "北京工业大学",
        postgraduate: "北京航空航天大学"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top {
  width: 100%;
  height: auto;
  background: url("../common/images/banner.jpg") no-repeat center 0px;
  background-size: cover;
  color: #fff;
}
.container {
  width: 100%;
  height: auto;
  background: url("../common/images/dott.png") repeat;
  position: relative;
}
.banner {
  max-width: 1200px;
  padding: 10% 0;
  margin: 0 auto;
}
.avator {
  float: left;
  width: 40%;
  text-align: center;
  position: relative;
  z-index: 10;
}
.avator img {
  width: 74%;
  border: 5px solid rgba(255, 255, 255, 0.68);
}
.info {
  float: right;
  width: 60%;
  text-align: left;
}
.info .hello {
  position: relative;
  display: inline-block;
  padding: 4px 16px;
  font-size: 25px;
  color: #fff;
  background-color: #03a9f4;
  font-family: "Overlock", cursive;
  vertical-align: top;
  box-shadow: 0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
/*小三角*/
.info .hello:after {
  position: absolute;
  width: 0;
  height: 0;
  left: 6px;
  bottom: -4px;
  content: "";
  border-style: solid;
  border-width: 6px 6px 0 6px;
  border-color: #03a9f4 transparent;
}
h1 {
  font-size: 40px;
  font-family: "Overlock", cursive;
}
h6 {
  margin-top: 6px;
  font-size: 20px;
  font-family: "Overlock", cursive;
  color: #c7c7c7;
  letter-spacing: 4px;
}
.info ul {
  margin-top: 10px;
  border-top: 1px solid #fff;
}
.info ul li {
  font-size: 25px;
  margin-top: 30px;
  font-family: "Overlock", cursive;
}
.info b {
  display: inline-block;
  font-family: "Overlock", cursive;
  margin-right: 10px;
}
.info ul li span:hover {
  color: #03a9f4;
  font-family: "Overlock", cursive;
}
#particles-js {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}
</style>
