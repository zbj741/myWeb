<template>
  <div class="project">
    <div class="container">
      <span class="tip">WHAT I DO</span>
      <h1 class="title">{{title}}</h1>
      <span class="border"></span>
      <!-- <ul>
        <li><img src="../common/images/web1.jpg" alt="项目1"></li>
        <li><img src="../common/images/web1.jpg" alt="项目2"></li>
        <li><img src="../common/images/web1.jpg" alt="项目3"></li>
        <li><img src="../common/images/web1.jpg" alt="项目4"></li>
        
      </ul> -->
      <ul>
        <li
          class="progress-bar"
          v-for="item in items"
          :key="item.message"
        >
          <div class = "ff">
            <div class="titlename">{{item.name}}</div>
            <div class="itemmessage">{{ item.message }}</div>
          </div>
        </li>
        <div class="clearfix"></div>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "project",
  data() {
    return {
      title: "我的项目",
      items: [
        {
          name: "基于区块链技术的应用平台设计与实现（国创、比赛 已经申请软著）",
          message:
            "此项目是基于区块链技术开发的彩票投注系统。采用的架构是Hyperledger Fabric联盟链 。本人主要负责后端智能合约的编写（Go语言实现）与部署，SDK开发以及前端应用node.js，express框架搭建网站。（约1500行）"
        },
        {
          name: "计算机博弈（比赛）",
          message:
            "此项目是以亚马逊棋为棋种的计算机零和博弈。本人主要负责估值部分的实现，走法生成的实现，以及搜索部分αβ剪枝的改进(加入了历史启发)。（约700行）"
        },
        {
          name: "利用Flex和Bison设计基于c的简单编译器（课设）",
          message:
            "在Linux环境下，使用Flex和Bison工具，设计并实现词法分析器、语法分析器以及语法制导的三地址代码生成器。（约1000行代码）"
        },
        {
          name: "基于区块链的药品溯源系统（毕设）",
          message:
            "使用Vue搭建前端展示页面，后端使用express框架作为服务器，连接mysql。底层使用Hyperledger Fabric1.3联盟链，其中智能合约用go语言编写，SDK调用使用node进行编写。（约3600行代码）"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.project {
  height: auto;
  width: 100%;
  margin: 0 auto;
  background-color: #fff;
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

ul {
  width: 100%;
  padding: 4% 0;
}
ul li {
  float: center;
  width: 100%;
  margin-right: 5%;
  height: 80%;
  box-sizing: border-box;
  transition: transform 0.25s ease;
}
ul li img {
  width: 100%;
  display: block;
}
.titlename {
  font-size: 25px;
  font-weight: bold;
}
.itemmessage {
  margin-top: 15px;
  font-size: 20px;
}
.ff {
  text-align:left;
  margin-bottom: 20px;
}
</style>
