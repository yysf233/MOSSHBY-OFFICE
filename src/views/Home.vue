<template>
  <div class="container">
    <!-- 轮播图 -->
    <el-carousel class="animate__animated animate__fadeInUp " height="600px" :interval="5000" arrow="always"
      indicator-position="none">
      <!-- <el-carousel-item v-for="(item, index) in imgData" :key="index">
        <div :style="{ 'background-image': 'url(' + 'image' + index + ');' }">
        </div>
      </el-carousel-item> -->
      <el-carousel-item>
        <div :style="'background-image:url(' + image0 + ');'">
        </div>
      </el-carousel-item>
      <el-carousel-item>
        <div :style="'background-image:url(' + image1 + ');'">
        </div>
      </el-carousel-item>
      <el-carousel-item>
        <div :style="'background-image:url(' + image2 + ');'">
        </div>
      </el-carousel-item>
    </el-carousel>
    <!-- 最新产品 -->
    <div class="new-product-wrap">
      <div class="line-wrap">
        <div class="line"></div>
        <div class="line-content">
          <p class="title">最新产品</p>
          <p>关注动态 改变自己</p>
          <div class="circle">
            <p></p>
            <p></p>
          </div>
        </div>
        <div class="line-right"></div>
      </div>
      <div class="swiper animate__animated animate__fadeInUp">
        <swiper :options="swiperOption" ref="mySwiper">
          <swiper-slide>I'm Slide 1</swiper-slide>
          <swiper-slide>I'm Slide 2</swiper-slide>
          <swiper-slide>I'm Slide 3</swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>

    </div>
    <!-- 预约流程 -->
    <div id="id0" class="reservation-process-wrap">
      <div class="line-wrap">
        <div class="line"></div>
        <div class="line-content">
          <p class="title">预约流程</p>
          <p>生活需要仪式感</p>
          <div class="circle">
            <p></p>
            <p></p>
          </div>
        </div>
        <div class="line-right"></div>
      </div>
      <div class="process-wrap">
        <div id="id1" class="process-content animate__repeat-2"><img src="../images/himo.33bce8bc.png">
          <div class="item-width " data-lazy-id="12">
            <p>Step1</p>
            <p class="process-name">关注海马体</p><span>关注海马体公众号了解最近上新产品</span><span class="line"></span>
          </div>
        </div>
        <div id="id2" class="process-content animate__repeat-2">
          <img src="../images/chooseStore.ebd559d3.png">
          <div class="item-width " data-lazy-id="14" style="transition-delay: 0.2s;">
            <p>Step2</p>
            <p class="process-name">确认产品</p><span>确认您预约的产品和拍摄门店</span><span class="line"></span>
          </div>
        </div>
        <div id="id3" class="process-content animate__repeat-2">
          <img src="../images/appointment.d0145d0f.png">
          <div class="item-width " data-lazy-id="16" style="transition-delay: 0.4s;">
            <p>Step3</p>
            <p class="process-name">预约时间</p><span>提前预约避免错过重要时刻</span><span class="line"></span>
          </div>
        </div>
        <div id="id4" class="process-content animate__repeat-2">
          <img src="../images/confirmOrder.09411bfb.png">
          <div class="item-width " data-lazy-id="18" style="transition-delay: 0.6s;">
            <p>Step4</p>
            <p class="process-name">确认下单</p><span>下单后期待最美的自己</span><span class="line"></span>
          </div>
        </div>
      </div>
    </div>
    <!-- HIMO标准服务 -->
    <div class="standard-service-wrap">
      <div class="line-wrap">
        <div class="line"></div>
        <div class="line-content">
          <p class="title">HIMO标准服务</p>
          <p>极致服务 最好的你</p>
          <div class="circle">
            <p></p>
            <p></p>
          </div>
        </div>
        <div class="line-right"></div>
      </div>
      <div class="tab-wrap">
        <ul>
          <li :class="{ active: isShow === true }" @click="handleTab(true)">
            <p href="#section-bar-0">海马体标准服务</p>
          </li>
          <li :class="{ active: isShow === false }" @click="handleTab(false)">
            <p href="#section-bar-1">大师店标准服务</p>
          </li>
        </ul>
        <div class="tab-content">
          <section v-show="isShow" class="tab-section active ">
            <div class="server-content animate__animated animate__fadeInUp"><img src="../images/photography.png">
              <p class="server-name">摄影</p>
              <p class="font-style">Photo</p><span>使用专业顶级的设备，统一培训的摄影师。给您全程微笑的服务，希望带给您一张机智的照片让一切舍不得忘掉的都留下来。</span>
            </div>
            <div class="server-content animate__delay-1s animate__animated animate__fadeInUp"
              style="transition-delay: 0.2s;" data-lazy-id="64"><img src="../images/makeup.png">
              <p class="server-name">化妆</p>
              <p class="font-style">Makeup</p><span>使用一线名牌化妆品所有化妆师经过专业培训，
                塑造饱满自信的状态，确保您的每一次上镜。</span>
            </div>
            <div class="server-content animate__delay-2s animate__animated animate__fadeInUp"
              style="transition-delay: 0.4s;" data-lazy-id="65"><img src="../images/clothing.png">
              <p class="server-name">服装</p>
              <p class="font-style">Dress</p><span>我们定期清洗每一件服装，确保干净整洁带有清香。我们专业定制，确保服装质量上乘，尺码齐全，样式丰富。</span>
            </div>
            <div class="server-content animate__delay-3s animate__animated animate__fadeInUp"
              style="transition-delay: 0.6s;" data-lazy-id="66"><img src="../images/ps.png">
              <p class="server-name">修图</p>
              <p class="font-style">PS</p><span>每个坐在您身边的修图师都经过专业培训，当面确认您的需求，注重效率与体验，iMAC电脑修图，以确保最优标准最高画质。</span>
            </div>
            <div class="server-content animate__delay-4s animate__animated animate__fadeInUp"
              style="transition-delay: 0.8s;" data-lazy-id="67"><img src="../images/print.png">
              <p class="server-name">冲印</p>
              <p class="font-style">Print</p><span>EPSIN Surelab
                系列高端商务用机位电压打印头专业影响及输出，带来私人杂志影像体验。</span>
            </div>
          </section>
          <section v-show="!isShow" class="tab-section active ">
            <div class="server-content animate__animated animate__fadeInUp"><img src="../images/marshalling.fa0e0b0d.png">
              <p class="server-name">视觉</p>
              <p class="font-style">Vision</p><span>启用全新金标LOGO,全套独家VI定制，带给你全新视觉体验。</span>
            </div>
            <div class="server-content animate__animated animate__fadeInUp animate__delay-1s  "><img
                src="../images/staff.c4b9a9e3.png">
              <p class="server-name">人员</p>
              <p class="font-style">Service</p><span>优选海马体工匠大师，经过全国统一培训，形象气质俱佳，统一黑金LOGO衬衫，享受尊贵服务。</span>
            </div>
            <div class="server-content animate__animated animate__fadeInUp animate__delay-2s "
              style="transition-delay: 0.4s;"><img src="../images/clothing.10b90e5d.png">
              <p class="server-name">服装</p>
              <p class="font-style">Dress</p><span>选用高端统一定制服装，尺码齐全，服装定期送洗，高频率更新更换，保证服装质感。</span>
            </div>
            <div class="server-content animate__animated animate__fadeInUp animate__delay-3s "
              style="transition-delay: 0.6s;"><img src="../images/makeup.96d6b5c7.png">
              <p class="server-name">化妆</p>
              <p class="font-style">Makeup</p><span>配备一线大牌化妆品、热门化妆单品，迪奥、香奈儿、雅诗兰黛、阿玛尼等一次性化妆用具，确保干净专一。</span>
            </div>
            <div class="server-content animate__animated animate__fadeInUp animate__delay-4s "
              style="transition-delay: 0.8s;"><img src="../images/space.c42043e6.png">
              <p class="server-name">空间</p>
              <p class="font-style">Space</p><span>刷新视觉嗅觉，顶级音响烘托，全套BOSE室内音响系统，airaroma室内香氛系统，专属海马体独有味道。</span>
            </div>
          </section>
        </div>
      </div>
    </div>
    <!-- 关于我们 -->
    <div class="about-us ">
      <div class="line-wrap">
        <div class="line"></div>
        <div class="line-content">
          <p class="title">关于我们</p>
          <p>极致服务 最好的你</p>
          <div class="circle">
            <p></p>
            <p></p>
          </div>
        </div>
        <div class="line-right"></div>
      </div>
      <div class="title">
        <h1>毛衫与白</h1>
      </div>
      <div class="introduction">
        <p>这里是毛衫与白摄影工作室,期待与您的合作! #街拍美女 #街头潮范儿 #人像摄影 #校园 #德州学院 </p>
      </div>
      <div class="content-cell pos-img">
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img @click="{}" src="../images/抖音.png" class="code-icon">
          <!-- </a> -->
          <!-- <div class="code douyin" ref="douyin">
            <img src="../images/douyin-code.png" alt="">
            <p class="code-attention">关注抖音</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/bilibili.png" class="code-icon">
          <!-- </a> -->
          <!-- <div class="code bilibili" ref="bilibili"><img src="../images/bilibili-code.png" alt="">
            <p class="code-attention">关注b站</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/小红书.png" class="code-icon">
          <!-- </a> -->
          <!-- <div class="code redbook" ref="addShow"><img src="../images/red-book-code.png" alt="">
            <p class="code-attention">关注小红书</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/公众号.png" class="code-icon">
          <!-- </a> -->
          <!-- <div class="code gongzhong" ref="addShow"><img src="../images/review-code.png" alt="">
            <p class="code-attention">关注公众号</p>
          </div> -->
        </div>
      </div>
    </div>
    <!-- footer -->
    <div class="footer-wrap">
      <div class="footer-content">
        <div class="company-logo"><img src="../images/毛衫与白LOGO.png" alt="">
        </div>
        <div class="whiteplace"></div>
        <div class="company-content">
          <div class="content">
            <div class="title">联系海马体</div>
            <p>400-068-5666</p>
          </div>
          <div class="company-code">
            <img src="../images/review-code.png" alt="">
            <p>扫码预约拍摄</p>
          </div>
        </div>

      </div>

      <div class="footer-bottom">
        <p>浙公网安备 33011802000662</p>
        <p><a href="https://beian.miit.gov.cn/" target="_blank" class="jump-page">浙ICP备11062584号-3</a></p>
      </div>
    </div>
  </div>
</template>
<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
import "../../public/css/swiper.min.css";
import image0 from '../images/banner1.jpg'
import image1 from '../images/banner1.jpg'
import image2 from '../images/banner1.jpg'
export default {
  name: 'Home',
  components: {
    swiper,
    swiperSlide,
  },
  data() {
    return {
      list: [1, 2, 3, 4],
      image0, image1, image2,
      arr: ['精致证件照', '职业形象照', '文艺照', '花颜照', '轻婚纱'],
      isShow: true,
      swiperOption: {
        loop: true,
        autoplay: {
          delay: 3000,
          stopOnLastSlide: false,
          disableOnInteraction: false
        },
        // 显示分页
        pagination: {
          el: ".swiper-pagination",
          clickable: true //允许分页点击跳转
        },
        // 设置点击箭头
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        },

      },
      bgImg: ['bg-img0', 'bg-img1', 'bg-img2'],
      imgData: ['bg-img0', 'bg-img1', 'bg-img2'],
    };
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    }
  },
  mounted() {
    // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
    console.log("this is current swiper instance object", this.swiper);
    window.addEventListener('scroll', this.scrollToTop);
  },
  methods: {
    handleTab(val) {
      this.isShow = val;
    }, scrollToTop() {
      // 获取视窗高度
      var domHight = document.body.offsetHeight;
      // dom滚动位置
      var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      // 获取监听元素
      var id;
      // 获取监听元素本身高度
      var scrollHeight;
      // 获取监听元素距离视窗顶部距离
      var offsetTop;
      // 获取监听元素距离顶部高度-窗口高度 
      var top;
      // 元素距离底部的高度+元素本身高度
      var bottom;
      this.list.map((i) => {
        id = document.getElementById(`id0`);
        scrollHeight = id.scrollHeight;
        offsetTop = id.offsetTop;
        top = offsetTop - domHight > 0 ? offsetTop - domHight : 0;
        bottom = scrollHeight + offsetTop;
        // 页面滚动位置 > 元素距离顶部高度-窗口高度 && 页面滚动位置 < 元素距离顶部高度+元素本身高度
        if (scrollTop >= top && scrollTop <= bottom) {
          let ele = document.getElementById(`id${i}`);
          if (i === 1) {
            ele.className = "process-content animate__animated animate__fadeInUp"
          } else {
            ele.className = `process-content animate__delay-${i - 1}s  animate__animated animate__fadeInUp`
          }
          console.log('元素出现在可视区');
        } else {
          console.log('元素不在可视区');
        }
      });
    },
  },
};

</script>

<style >
.animate__delay-1s {
  --animate-delay: 0.05s;
}

.animate__delay-2s {
  --animate-delay: 0.1s;
}

.animate__delay-3s {
  --animate-delay: 0.15s;
}

.animate__delay-4s {
  --animate-delay: 0.17s;
}

.animate__delay-5s {
  --animate-delay: 0.22s;
}

/* 轮播图 */
.fade-enter-active,
.fade-leave-active {
  transition: opacity .05s
}

.fade-enter,
.fade-leave-to {
  opacity: 0
}

.item-title {
  background: center no-repeat
}

.el-carousel__item {
  background-position: center top;
}

.el-carousel__item:nth-of-type(1) {
  background-image: url(../images/banner1.jpg);
}

.el-carousel__item:nth-of-type(2) {
  background-image: url(../images/banner2.jpg);
}

.el-carousel__item:nth-of-type(3) {
  background-image: url(../images/banner3.jpg);
}

.el-carousel__container .el-carousel__arrow {
  background-color: rgba(135, 135, 135, 0.15);
  width: 6%;
  height: 10%;
  top: 95%;

}

.el-carousel__arrow i {
  font-size: 30px;
  font-weight: 600;
  color: rgb(34, 34, 34);
}

.el-carousel__container .el-carousel__arrow--left {
  border-radius: 5px 0 0 5px;
  left: 44%;
}

.el-carousel__container .el-carousel__arrow:hover {
  background-color: rgba(135, 135, 135, 0.4);
}

.el-carousel__container .el-carousel__arrow--right {
  border-radius: 0 5px 5px 0;
  right: 44%;
}

/* 最新产品 */
.new-product-wrap {
  padding: 90px 0 20px;
}

.about-us .line-wrap,
.standard-service-wrap .line-wrap,
.new-product-wrap .line-wrap,
.reservation-process-wrap .line-wrap {
  width: 1152px;
  margin: 0 auto;
  position: relative;
}

.new-product-wrap .swiper {
  position: relative;
}

.swiper-container {
  position: relative;
  width: 100%;
  height: 200px;
  background: pink;
}

.swiper-container .swiper-slide {
  width: 100%;
  line-height: 200px;
  background: yellowgreen;
  color: #000;
  font-size: 16px;
  text-align: center;
}

.line-wrap .line,
.line-wrap .line-right {
  position: absolute;
  top: 45px;
  width: 25%;
  height: 1px;
  background-color: #ebebeb;
  display: inline-block
}

.line-wrap .line {
  left: 0;
}

.line-wrap .line-right {
  right: 0;
}

.line-wrap .line-content {
  width: 100%;
  display: inline-block;
  vertical-align: middle;
  margin: 0 auto;
  text-align: center;
}

.line-wrap .line-content .title {
  padding-bottom: 4px;
  color: #16161a;
  font-size: 24px;
  font-weight: 600;
}

.line-wrap .line-content p {
  padding-bottom: 3px;
  color: #919199;
  font-size: 14px;
}

.line-content .circle {
  padding-top: 4px;
}

.line-wrap .line-content .circle p {
  width: 16px;
  height: 16px;
  background-color: #48ce55;
  border-radius: 50%;
  display: inline-block;
}

.line-wrap .line-content p {
  padding-bottom: 3px;
  color: #919199;
  font-size: 14px;
}

.line-wrap .line-content p:last-child {
  background-color: #000;
  margin-left: 4px;
}

/* 预约流程 */
.reservation-process-wrap {
  padding: 80px 0px;
  background-color: #fafafa;
}

.reservation-process-wrap .process-wrap {
  width: 1152px;
  margin: 60px auto 0;
}

.reservation-process-wrap .process-wrap .process-content {
  position: relative;
  display: inline-block;
  vertical-align: top;
  width: 25%;
}

.reservation-process-wrap .process-wrap .process-content:first-child:before {
  right: -78px;
}

.reservation-process-wrap .process-wrap .process-content:before {
  position: absolute;
  content: "";
  width: 120px;
  height: 1px;
  background-color: #d8d8d8;
  top: 543px;
  right: -74px;
}

.reservation-process-wrap .process-wrap .process-content .item-width,
.reservation-process-wrap .process-wrap .process-content img {
  width: 320px;
  text-align: center;
  margin: 0;
}

.reservation-process-wrap .process-wrap .process-content p {
  font-size: 20px;
  color: #45454d;
  font-weight: 600;
}

.reservation-process-wrap .process-wrap .process-content .process-name {
  font-weight: 400;
}

.reservation-process-wrap .process-wrap .process-content p {
  font-size: 20px;
  color: #45454d;
  font-weight: 600;
}

.reservation-process-wrap .process-wrap .process-content .process-name:after {
  content: "";
  display: block;
  width: 32px;
  height: 1px;
  margin: 8px auto 14px;
  background-color: #000;
}

.reservation-process-wrap .process-wrap .process-content span {
  font-size: 13px;
  color: #919199;
}

.reservation-process-wrap .process-wrap .process-content span {
  font-size: 13px;
  color: #919199;
}

/* HIMO标准服务 */
.tab-wrap {
  margin-top: 34px;

}

.server-content {
  text-align: center;
}

.tab-wrap ul {
  text-align: center;
}

.tab-wrap ul li {
  display: inline-block;
  padding: 16px 90px;
  border: 1px solid #d4d4d9;
  border-radius: 2px 0 0 2px;
  font-size: 14px;
  color: #45454d;
}

.tab-wrap ul li.active:last-child {
  border: 1px solid #c5a563;
  background-color: #c5a563;
  color: #fff;
}

.tab-wrap ul li.active {
  border: 1px solid #000;
  background-color: #000;
  color: #fff;
}

.tab-wrap ul li:last-child {
  border-radius: 0 2px 2px 0;
}

.tab-wrap .tab-content {
  width: 1152px;
  margin: 60px auto 0;
}

.tab-wrap .tab-content .tab-section.active {
  display: block;
  -webkit-transition: all 2s;
  transition: all 2s;
}

.tab-wrap .tab-content .tab-section {
  display: none;
}

.tab-wrap .tab-content .tab-section .server-content {
  display: inline-block;
  width: 20%;
  height: 384px;
  vertical-align: top;
}

.lazy-animate-init.lazy-animate-run {
  -webkit-transition: opacity .5s linear, -webkit-transform .5s ease;
  transition: opacity .5s linear, -webkit-transform .5s ease;
  transition: transform .5s ease, opacity .5s linear;
  transition: transform .5s ease, opacity .5s linear, -webkit-transform .5s ease;
  visibility: visible;
  opacity: 1;
  -webkit-transform: none;
  transform: none;
}

.lazy-animate-init {
  visibility: hidden;
  -webkit-transform: translateY(50px);
  transform: translateY(50px);
  opacity: 0;
}

.tab-wrap .tab-content .tab-section .server-content img {
  width: 211px;
}

.tab-wrap .tab-content .tab-section img {
  width: 100%;
}

.tab-wrap .tab-content .tab-section .server-content .server-name {
  font-size: 24px;
  font-weight: 600;
  color: #16161a;
  padding: 20px 0 2px;
}

.tab-wrap .tab-content .tab-section .server-content p {
  padding-bottom: 14px;
  font-size: 14px;
  font-family: IBMPlexSansBold;
  color: #d4d4d9;
}

.tab-wrap .tab-content .tab-section .server-content .font-style {
  font-style: oblique;
}

.tab-wrap .tab-content .tab-section .server-content p {
  padding-bottom: 14px;
  font-size: 14px;
  font-family: IBMPlexSansBold;
  color: #d4d4d9;
}

.tab-wrap .tab-content .tab-section .server-content span {
  display: inline-block;
  width: 187px;
  color: #45454d;
  font-size: 13px;
}

.tab-wrap .tab-content .tab-section img {
  margin: 0;
}

.new-product-wrap,
.standard-service-wrap {
  background-color: #fff;
  padding: 80px 0px;
}



.about-us {
  background-color: #fafafa;
  padding: 80px 0px;
}

.about-us .title h1,
.about-us .introduction p {
  text-align: center;
  margin-bottom: 50px;
}

.lazy-animate-init.lazy-animate-run {
  -webkit-transition: opacity .5s linear, -webkit-transform .5s ease;
  transition: opacity .5s linear, -webkit-transform .5s ease;
  transition: transform .5s ease, opacity .5s linear;
  transition: transform .5s ease, opacity .5s linear, -webkit-transform .5s ease;
  visibility: visible;
  opacity: 1;
  -webkit-transform: none;
  transform: none;
}

.content-cell {
  display: flex;
  flex-wrap: wrap;
  width: 65%;
  margin: 0 auto;
  text-align: center;
  font-size: 12px;
  color: #919199;
  cursor: pointer;
}

.code-content {
  width: 50%;
  height: 80px;
  /* margin-top: 50px; */
}

.pos-img .code-content .code-icon {
  width: 150px;
}

/* 
.content-cell img {
  display: inline-block;
} */

/* .pos-img .code-content .code {
  width: 174px;
  height: 190px;
  background-size: 100%;
  background-repeat: no-repeat;
  opacity: 0;
  z-index: -1;
  position: absolute;
} */

/* .pos-img .code-content .douyin,
.pos-img .code-content .bilibili,
.pos-img .code-content .redbook,
.pos-img .code-content .gongzhong {
  position: absolute;
  bottom: 0;
  right: 100px;
} */

/* .pos-img .code-content .code img {
  width: 140px;
  height: 140px;
  margin-top: 16px;
} */

.content-cell img {
  display: inline-block;
}

/* 
.pos-img .code-content .code .code-attention {
  color: #16161a;
} */

/* .pos-img .code-content .code p {
  text-align: center;
  margin-top: 50px;
}

.code-content:hover .code {
  opacity: 1;
  z-index: 1;
} */

/* footer */
.footer-wrap {
  width: 100%;
  background-color: #fafafa;
  border-top: 1px solid #e3e3e6;
}

.footer-wrap .footer-content {
  display: flex;
  margin: 24px auto;
  width: 80%;
  /* height: 120px; */
  /* margin: 0 auto 62px; */
  /* padding-top: 48px; */
}

.footer-wrap .footer-content .company-logo {
  flex: 1;
}

.footer-wrap .footer-content .company-logo img {
  width: 150px;
  background-color: green;
  margin: 0;
}

.footer-wrap .footer-content .whiteplace {
  flex: 1;
}

.footer-wrap .footer-content .company-content {
  flex: 2;
  display: flex;
}

.footer-wrap .footer-content .company-content .content {
  flex: 1;
  text-align: center;
  font-size: 28px;
  font-weight: 500;

}

.footer-wrap .footer-content .company-content .company-code {
  flex: 1;
}

.footer-wrap .footer-content .company-code img {
  width: 100px;
  margin: 0 auto;
  display: block;
}

.footer-wrap .footer-content .company-code p {
  font-size: 14px;
  font-weight: 400;
  color: #45454d;
  text-align: center;
}

.footer-wrap .footer-bottom p:first-child:after {
  display: inline-block;
  content: "";
  height: 18px;
  width: 1.5px;
  background-color: #919199;
  vertical-align: bottom;
  margin: 0 18px;
}

.footer-bottom {
  text-align: center;
  background-color: #f0f0f2;
  color: #919199;
  font-size: 16px;
  padding: 8px 0;
}

.footer-wrap .footer-bottom p {
  display: inline-block;
}

.footer-bottom p .jump-page {
  color: #919199;
  text-decoration: none;
}
</style>