<template>
  <div class="skill">
    <div class="container">
      <span class="tip">WHAT I HONOURED</span>
      <h1 class="title">{{title}}</h1>
      <span class="border"></span>
      <div class="s_wrapper">
        <ul>
          <li
            class="progress-bar"
            v-for="item in items"
            :key="item.message"
          >
            {{item.time}}{{ item.message }}
          </li>
        </ul>
        <div class="clearfix"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "awarded",
  data() {
    return {
      title: "荣获奖项",
      items: [
        { message: "第十二届ICAN国际创新创业大赛北京市三等奖", time :"2018.09"},
        { message: "第一届“中国软件杯”双创大赛全国二等奖", time :"2018.08"},
        { message: "软著：《基于区块链技术的彩票投注系统》", time :"2018.06"},
        { message: "中国大学生计算机设计大赛北京市三等奖", time :"2018.05"},
        { message: "美国大学生数学建模竞赛全国二等奖", time :"2018.04"},
        { message: "第九届蓝桥杯C/C++程序设计北京市三等奖", time :"2018.04"},
        { message: "第九届蓝桥杯软件创业团队赛优秀奖", time :"2018.04"},
        { message: "第十一届中国计算机博弈锦标赛全国一等奖", time :"2017.07"},
        { message: "全国大学生数学建模竞赛北京市二等奖", time :"2017.10"},
        { message: "北京工业大学三好学生", time :"2017.10"},
        { message: "北京工业大学科技创新奖", time :"2016.10"},
        { message: "北京工业大学学习优秀奖", time :"2016.10 2017.10"}
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skill {
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

.progress-bar {
  float: left;
  width: 100%;
  height: auto;
  padding: 0 40px;
  box-sizing: border-box;
  margin-top: 10px;
  font-size: 20px;
}
</style>
