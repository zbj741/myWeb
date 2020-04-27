<template>
  <div class="experience">
    <div class="container">
      <span class="tip">WHERE I WORKED</span>
      <h1 class="title">{{title}}</h1>
      <span class="border"></span>
      <ul class="content">
        <li>
          <div class="content_left tx_right">
            <span class="s1"></span>
            <h4> 2018.08 - 2018.09</h4>
          </div>
          <div class="content_right tx_left">
            <h4>北京科易动力有限公司（学校实习）</h4>
            <p>一个月内独自完成科易动力实验的排程系统，典型的B/S架构，前端使用html、css、JavaScript动态网页，后端使用jsp进行逻辑处理，用java访问数据库。</p>
          </div>
          <div class="clearfix"></div>
        </li>
        <li>
          <div class="content_left tx_right">
            <span class="s2"></span>
            <h4>2018.09-2018.12 </h4>
          </div>
          <div class="content_right tx_left">
            <h4>北京智链万源 </h4>
            <p>1.基于hyperledger fabric平台的系统研究，改写官方例子first-network。</p>
            <p>2.学习PBFT算法，同态加密过程。以及使用压力测试工具Caliper，修改Caliper智能合约。</p>
            <p>3.调研金融版区块链底层平台bcos、fisco-bcos区块链，撰写调研报告。</p>
            <p>4.在fisco-bcos平台搭建药品溯源demo，前端用微信小程序进行交互，后端用node express框架起webserver与fisco-bcos区块链网络进行数据交互。
            </p>
          </div>
          <div class="clearfix"></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "internExperience",
  data() {
    return {
      title: "实习经历"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.experience {
  height: auto;
  width: 100%;
  margin: 0 auto;
  background-color: #f5f5f5;
  text-align: center;
}
.container {
  height: auto;
  max-width: 1200px;
  margin: 0 auto;
  padding: 4% 0;
}
.tip {
  display: inline-block;
  position: relative;
  padding: 6px 20px;
  margin: 0 auto 10px;
  font-size: 20px;
  background: #03a9f4;
  color: #fff;
}
.tip:after {
  position: absolute;
  width: 0;
  height: 0;
  left: 42%;
  bottom: -10px;
  content: "";
  border-style: solid;
  border-width: 10px 10px 0 10px;
  border-color: #03a9f4 transparent;
}
.title {
  padding: 6px 0 10px;
  font-family: "Overlock", cursive;
  color: #2f2c06;
  font-size: 36px;
}
.border {
  display: block;
  width: 20%;
  height: 1px;
  position: relative;
  margin: 0 auto 30px;
  background: #8c8989;
}
.border:after {
  position: absolute;
  top: 0;
  left: 30%;
  content: " ";
  width: 40%;
  height: 5px;
  margin-top: -2px;
  background: #03a9f4;
}

ul.content {
  padding-top: 20px;
}
ul.content li {
  font-size: 20px;
  color: #999;
  position: relative;
}
.content_left {
  width: 50%;
  float: left;
  padding: 25px 6% 0 0;
}
.content_left h4 {
  text-align: center;
  position: relative;
  padding: 10px 40px;
  font-size: 20px;
  color: #fff;
  background-color: #1b242f;
}
/* 绝对定位居中，如果在没有固定高度宽度的盒子里，不要使用百分比定位，使用px，rem，居中用50%+margin负值 */
.content_left h4:before {
  width: 0;
  height: 0;
  position: absolute;
  top: 50%;
  margin-top: -6px;
  right: -10px;
  content: "";
  border-style: solid;
  border-width: 6px 0 6px 10px;
  border-color: transparent transparent transparent #1b242f;
}
.content_right {
  width: 50%;
  float: left;
  padding: 20px 0 10px 6%;
}
.content_right h4 {
  text-align: center;
  padding: 10px 50px;
  margin-bottom: 6px;
  font-size: 20px;
  border: 1px solid #d4d4d4;
  color: #1b242f;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.175);
}
.content_right p {
  line-height: 35px;
  font-size: 20px;
}
/*小图标*/
ul.content li span {
  position: absolute;
  top: 30px;
  right: -19px;
  z-index: 10;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: url("../common/images/icon.png") no-repeat center;
  background-size: 50%;
}
ul.content li .s1 {
  background-color: #44c7f4;
}
ul.content li .s2 {
  background-color: #eb5424;
}

.tx_left {
  position: relative;
  text-align: left;
  box-sizing: border-box;
  border-left: 1px solid #999;
}
.tx_right {
  position: relative;
  text-align: right;
  box-sizing: border-box;
}
</style>
