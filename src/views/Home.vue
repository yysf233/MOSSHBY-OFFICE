
<template>
  <div class="container">
    <div id="wrap" :style="{ height: screenHeight + 'px' }">
      <div id="main" :style="{ top: nowTop + 'px' }">
        <div id="pageUl">
          <div class="aaa">
            <ul type="circle">
              <li
                @click="navTo(1, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 1 }"
              >
                1
              </li>
              <li
                @click="navTo(2, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 2 }"
              >
                2
              </li>
              <li
                @click="navTo(3, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 3 }"
              >
                3
              </li>
              <li
                @click="navTo(4, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 4 }"
              >
                4
              </li>
              <li
                @click="navTo(5, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 5 }"
              >
                5
              </li>
              <li
                @click="navTo(6, $event)"
                class="rightTreeText"
                :class="{ textActive: curIndex == 6 }"
              >
                6
              </li>
            </ul>
            <!-- <div class="homeLine"></div> -->
            <ul type="circle" title="point">
              <div
                @click="navTo(1, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 1 }"
              >
                <li class="whiteRound"></li>
              </div>
              <div
                @click="navTo(2, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 2 }"
              >
                <li class="whiteRound"></li>
              </div>
              <div
                @click="navTo(3, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 3 }"
              >
                <li class="whiteRound"></li>
              </div>
              <div
                @click="navTo(4, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 4 }"
              >
                <li class="whiteRound"></li>
              </div>
              <div
                @click="navTo(5, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 5 }"
              >
                <li class="whiteRound"></li>
              </div>
              <div
                @click="navTo(6, $event)"
                class="whiteRoundBorder"
                :class="{ active: curIndex == 6 }"
              >
                <li class="whiteRound"></li>
              </div>
            </ul>
          </div>
        </div>
        <div
          style="
            background-color: #1b6d85;
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page1"
          class="page"
        >
          1
        </div>
        <div
          style="
            background-color: #5cb85c;
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page2"
          class="page"
        >
          2
        </div>
        <div
          style="
            background-color: #8a6d3b;
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page3"
          class="page"
        >
          3
        </div>
        <div
          style="
            background-color: #337ab7;
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page4"
          class="page"
        >
          4
        </div>
        <div
          style="
            background-color: #66512c;
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page5"
          class="page"
        >
          5
        </div>
        <div
          style="
            background-color: rgb(255, 179, 32);
            font-size: 46px;
            color: #fff;
            text-align: center;
          "
          id="page5"
          class="page"
        >
          6
          <div class="wrapper">
            <Footer />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'
export default {
  components: {
    Footer
  },
  name: 'home',
  data () {
    return {
      screenWeight: 0, // 屏幕宽度
      screenHeight: 0, // 屏幕高度
      index: 1, // 用于判断翻页
      curIndex: 1, // 当前页的index
      startTime: 0, // 翻屏起始时间
      endTime: 0, // 上一次翻屏结束时间
      nowTop: 0, // 翻屏后top的位置
      pageNum: 0, // 一共有多少页
      main: Object,
      obj: Object
    }
  },
  mounted () {
    this.screenWeight = document.documentElement.clientWidth
    this.screenHeight = document.documentElement.clientHeight
    this.main = document.getElementById('main')
    this.obj = document.getElementsByTagName('div')
    for (let i = 0; i < this.obj.length; i++) {
      if (this.obj[i].className === 'page') {
        this.obj[i].style.height = this.screenHeight + 'px'
      }
    }
    this.pageNum = document.querySelectorAll('.page').length

    // 浏览器兼容
    if (navigator.userAgent.toLowerCase().indexOf('firefox') !== -1) {
      document.addEventListener('DOMMouseScroll', this.scrollFun, false)
    } else if (document.addEventListener) {
      document.addEventListener('mousewheel', this.scrollFun, false)
    } else if (document.attachEvent) {
      document.attachEvent('onmousewheel', this.scrollFun)
    } else {
      document.onmousewheel = this.scrollFun
    }
  },
  methods: {
    navTo (a) {
      console.log(this.index)
      console.log('a', a)
      this.index = a
      this.toPage(a)
      this.active = a
      console.log(this.active)
    },
    scrollFun (event) {
      this.startTime = new Date().getTime()
      // mousewheel事件中的 “event.wheelDelta” 属性值：返回的如果是正值说明滚轮是向上滚动
      // DOMMouseScroll事件中的 “event.detail” 属性值：返回的如果是负值说明滚轮是向上滚动
      const delta = event.detail || -event.wheelDelta
      // 如果当前滚动开始时间和上次滚动结束时间的差值小于1.5s，则不执行翻页动作，这样做是为了实现类似节流的效果
      if (this.startTime - this.endTime > 1500) {
        if (
          delta > 0 &&
          parseInt(this.main.offsetTop) >=
            -(this.screenHeight * (this.pageNum - 2))
        ) {
          // 向下滚动
          this.index++
          this.toPage(this.index)
        } else if (delta < 0 && parseInt(this.main.offsetTop) < 0) {
          // 向上滚动
          this.index--
          this.toPage(this.index)
        }
        // 本次翻页结束，记录结束时间，用于下次判断
        this.endTime = new Date().getTime()
      }
    },
    // 翻页
    toPage (index) {
      if (index !== this.curIndex) {
        const delta = index - this.curIndex
        this.nowTop = this.nowTop - delta * this.screenHeight
        this.curIndex = index
      }
    }
  }
}
</script>
<style>
html,
body {
  height: 100%;
}

body,
ul,
li,
a,
p,
div {
  /*慎删*/
  padding: 0px;
  margin: 0px;
}

ul,
li {
  list-style: none;
}

#wrap {
  overflow: hidden;
  width: 100%;
}

.homeLine {
  width: 0.01rem;
  height: 4.86rem;
  background: linear-gradient(
    244deg,
    rgba(255, 255, 255, 0) 0%,
    rgba(255, 255, 255, 1) 50%,
    rgba(255, 255, 255, 0) 100%
  );
  margin: 0 10px;
}

#main {
  position: relative;
  transition: top 1.5s;
}

.page {
  /*谨删*/
  width: 100%;
  margin: 0;
}

#pageUl {
  position: fixed;
  right: 10px;
}

.aaa {
  top: 50%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  position: fixed;
  right: 30px;
}

[title="point"] li {
  font-size: 30px;
  border-radius: 4px;
  list-style: none;
}

/* 页面样式 */
.whiteRoundBorder {
  padding: 5px;
  border: 1px solid red transparent;
  margin-bottom: 10px;
}

.whiteRound {
  width: 4px;
  height: 4px;
  background: rgba(255, 255, 255, 0.4);
}

.active li {
  border: 1px solid rgb(255, 255, 255);
  border-radius: 4px;
  background: rgb(255, 255, 255);
}

.rightTreeText {
  font-size: 14px;
  font-family: PingFangSC-Medium, PingFang SC;
  font-weight: 500;
  color: rgba(255, 255, 255, 0.6);
  margin-bottom: 7px;
}

.textActive {
  font-size: 14px;
  font-family: PingFangSC-Medium, PingFang SC;
  font-weight: 500;
  color: rgba(255, 255, 255, 1);
}
</style>
