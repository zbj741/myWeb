<template>
  <div class="about">
    <div class="container">
      <span class="tip">WHO AM I</span>
      <h1 class="title">{{title}}</h1>
      <span class="border one"></span>
      <div class="a_info">
        <swiper
          :options="swiperOption"
          ref="mySwiper"
        >
          <!-- slides -->
          <swiper-slide>
            <p>本人性格开朗，待人友善，为人真诚，工作细致，认真负责。抗压能力、学习能力强。</p>
          </swiper-slide>
          <swiper-slide>
            <p>熟悉区块链的各种共识算法（POW、POS、DPOS、PBFT等）。</p>
          </swiper-slide>
          <swiper-slide>
            <p>可以手动配置并启动部署Hyperledger Fabric网络，编写智能合约、node sdk交互等。</p>
          </swiper-slide>
          <swiper-slide>
            <p>了解Hadoop中分布式存储HDFS细节及过程，以及MapReduce计算框架过程。</p>
          </swiper-slide>
          <div
            class="swiper-pagination"
            slot="pagination"
          ></div>
          <div
            class="swiper-button-prev"
            slot="button-prev"
          ></div>
          <div
            class="swiper-button-next"
            slot="button-next"
          ></div>
        </swiper>
      </div>
    </div>
  </div>
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "about",
  data() {
    return {
      title: "自我简述",
      swiperOption: {
        spaceBetween: 30,
        centeredSlides: true,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.about {
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
.a_info {
  font-size: 20px;
}
.swiper-container {
  width: 100%;
  height: 300px;
  line-height: 300px;
  overflow: hidden;
  text-align: center;
}
.swiper-pagination {
  top: 46%;
}
</style>
