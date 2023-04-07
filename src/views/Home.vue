<template>
  <div class="container">
    <!-- 轮播图 -->
    <div class="main">
      <el-carousel
        class="animate__animated animate__fadeInUp"
        height="600px"
        :interval="5000"
        arrow="always"
        indicator-position="none"
      >
        <!-- <el-carousel-item v-for="(item, index) in imgData" :key="index">
        <div :class="item">
        </div>
      </el-carousel-item> -->
        <el-carousel-item>
          <div :style="'background-image:url(' + image0 + ');'"></div>
        </el-carousel-item>
        <el-carousel-item>
          <div :style="'background-image:url(' + image1 + ');'"></div>
        </el-carousel-item>
        <el-carousel-item>
          <div :style="'background-image:url(' + image2 + ');'"></div>
        </el-carousel-item>
      </el-carousel>
    </div>
    <!-- 最新产品 -->
    <div class="new-product-wrap" style="padding: 80px 0">
      <div class="line-wrap">
        <div class="line" style="left: 10%"></div>
        <div class="line-content">
          <p class="title">最新产品</p>
          <p>关注动态 改变自己</p>
          <div class="circle">
            <p></p>
            <p></p>
          </div>
        </div>
        <div class="line-right" style="right: 15%"></div>
      </div>
      <!-- 轮播图 -->
      <div class="block" style="display: flex; width: 100%">
        <div style="width: 30%; background-color: #fff; z-index: 9999"></div>
        <el-carousel
          class="new-product"
          trigger="click"
          :autoplay="false"
          indicator-position="outside"
          arrow="always"
          height="44rem"
        >
          <el-carousel-item label="精致证件照">
            <img
              id="id111"
              src="http://www.haimati.cn/img/certificate.f4f704b7.png"
              class=""
            />
            <div id="newproduct">
              <p class="title">精致证件照</p>
              <p class="tip">
                一张精致的证件照，能让你的生活焕然一新，能为你的生活带来意想不到的改变
              </p>
              <div class="detail-btn">
                <p>查看详情</p>
              </div>
            </div>
          </el-carousel-item>
          <el-carousel-item label="职业形象照">
            <img src="http://www.haimati.cn/img/occupation.8a243d1b.png" />

            <div
              id="newest"
              class="lazy-animate-init lazy-animate-run"
              data-lazy-id="3"
              style="transition-delay: 0.4s"
            >
              <p class="title">职业形象照</p>
              <p class="tip">
                职场中，专业干练的职业形象展示，对您的事业至关重要。职业形象照，展现你的职业态度和专业气质。
              </p>
              <div class="detail-btn">
                <p>查看详情</p>
              </div>
            </div>
          </el-carousel-item>
          <el-carousel-item label="文艺照">
            <img src="http://www.haimati.cn/img/literary.f2ae8108.png" />

            <div
              class="lazy-animate-init lazy-animate-run"
              data-lazy-id="5"
              style="transition-delay: 0.7s"
            >
              <p class="title">文艺照</p>
              <p class="tip">
                用表情和神态表达你的个性，用镜头和照片定格下你张扬的宣言。
              </p>
              <div class="detail-btn">
                <p>查看详情</p>
              </div>
            </div>
          </el-carousel-item>
          <el-carousel-item label="花颜照">
            <img src="http://www.haimati.cn/img/flower-face.2bc065ce.png" />

            <div
              class="lazy-animate-init lazy-animate-run"
              data-lazy-id="7"
              style="transition-delay: 1s"
            >
              <p class="title">花颜照</p>
              <p class="tip">春回梦醒，潋滟一身花色</p>
              <div class="detail-btn">
                <p>查看详情</p>
              </div>
            </div>
          </el-carousel-item>
          <el-carousel-item label="轻婚纱">
            <img src="http://www.haimati.cn/img/wedding.fc9fc233.png" />

            <div
              class="lazy-animate-init lazy-animate-run"
              data-lazy-id="9"
              style="transition-delay: 1.3s"
            >
              <p class="title">轻婚纱</p>
              <p class="tip">穿上婚纱，向你展示我一生最美的模样</p>
              <div class="detail-btn">
                <p>查看详情</p>
              </div>
            </div>
          </el-carousel-item>
        </el-carousel>
        <div style="width: 30%; background-color: #fff; z-index: 9998"></div>
      </div>
    </div>
    <!-- 预约流程 -->
    <div id="id0" class="padding reservation-process-wrap">
      <div class="line-wrap animate__animated animate__fadeInUp">
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
        <div id="id1" class="process-content animate__repeat-2">
          <img src="../images/himo.33bce8bc.png" />
          <div class="item-width" data-lazy-id="12">
            <p>Step1</p>
            <p class="process-name">关注海马体</p>
            <span>关注海马体公众号了解最近上新产品</span
            ><span class="line"></span>
          </div>
        </div>
        <div id="id2" class="process-content animate__repeat-2">
          <img src="../images/chooseStore.ebd559d3.png" />
          <div
            class="item-width"
            data-lazy-id="14"
            style="transition-delay: 0.2s"
          >
            <p>Step2</p>
            <p class="process-name">确认产品</p>
            <span>确认您预约的产品和拍摄门店</span><span class="line"></span>
          </div>
        </div>
        <div id="id3" class="process-content animate__repeat-2">
          <img src="../images/appointment.d0145d0f.png" />
          <div
            class="item-width"
            data-lazy-id="16"
            style="transition-delay: 0.4s"
          >
            <p>Step3</p>
            <p class="process-name">预约时间</p>
            <span>提前预约避免错过重要时刻</span><span class="line"></span>
          </div>
        </div>
        <div id="id4" class="process-content animate__repeat-2">
          <img src="../images/confirmOrder.09411bfb.png" />
          <div
            class="item-width"
            data-lazy-id="18"
            style="transition-delay: 0.6s"
          >
            <p>Step4</p>
            <p class="process-name">确认下单</p>
            <span>下单后期待最美的自己</span><span class="line"></span>
          </div>
        </div>
      </div>
    </div>
    <!-- HIMO标准服务 -->
    <div class="padding standard-service-wrap">
      <div class="line-wrap animate__animated animate__fadeInUp">
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
      <div class="tab-wrap animate__animated animate__fadeInUp">
        <ul>
          <li
            class="btn1"
            :class="{ active: isShow === true }"
            @click="handleTab(true)"
          >
            <p href="#section-bar-0">海马体标准服务</p>
          </li>
          <li
            class="btn2"
            :class="{ active: isShow === false }"
            @click="handleTab(false)"
          >
            <p href="#section-bar-1">大师店标准服务</p>
          </li>
        </ul>
        <div class="tab-content">
          <section v-show="isShow" class="tab-section active black">
            <div class="server-content animate__animated animate__fadeInUp">
              <img src="../images/photography.png" />
              <p class="server-name">摄影</p>
              <p class="font-style">Photo</p>
              <span
                >使用专业顶级的设备，统一培训的摄影师。给您全程微笑的服务，希望带给您一张机智的照片让一切舍不得忘掉的都留下来。</span
              >
            </div>
            <div
              class="server-content animate__delay-1s animate__animated animate__fadeInUp"
              style="transition-delay: 0.2s"
              data-lazy-id="64"
            >
              <img src="../images/makeup.png" />
              <p class="server-name">化妆</p>
              <p class="font-style">Makeup</p>
              <span
                >使用一线名牌化妆品所有化妆师经过专业培训，
                塑造饱满自信的状态，确保您的每一次上镜。</span
              >
            </div>
            <div
              class="server-content animate__delay-2s animate__animated animate__fadeInUp"
              style="transition-delay: 0.4s"
              data-lazy-id="65"
            >
              <img src="../images/clothing.png" />
              <p class="server-name">服装</p>
              <p class="font-style">Dress</p>
              <span
                >我们定期清洗每一件服装，确保干净整洁带有清香。我们专业定制，确保服装质量上乘，尺码齐全，样式丰富。</span
              >
            </div>
            <div
              class="server-content animate__delay-3s animate__animated animate__fadeInUp"
              style="transition-delay: 0.6s"
              data-lazy-id="66"
            >
              <img src="../images/ps.png" />
              <p class="server-name">修图</p>
              <p class="font-style">PS</p>
              <span
                >每个坐在您身边的修图师都经过专业培训，当面确认您的需求，注重效率与体验，iMAC电脑修图，以确保最优标准最高画质。</span
              >
            </div>
            <div
              class="server-content animate__delay-4s animate__animated animate__fadeInUp"
              style="transition-delay: 0.8s"
              data-lazy-id="67"
            >
              <img src="../images/print.png" />
              <p class="server-name">冲印</p>
              <p class="font-style">Print</p>
              <span
                >EPSIN Surelab
                系列高端商务用机位电压打印头专业影响及输出，带来私人杂志影像体验。</span
              >
            </div>
          </section>
          <section v-show="!isShow" class="tab-section active golden">
            <div class="server-content animate__animated animate__fadeInUp">
              <img src="../images/marshalling.fa0e0b0d.png" />
              <p class="server-name">视觉</p>
              <p class="font-style">Vision</p>
              <span>启用全新金标LOGO,全套独家VI定制，带给你全新视觉体验。</span>
            </div>
            <div
              class="server-content animate__animated animate__fadeInUp animate__delay-1s"
            >
              <img src="../images/staff.c4b9a9e3.png" />
              <p class="server-name">人员</p>
              <p class="font-style">Service</p>
              <span
                >优选海马体工匠大师，经过全国统一培训，形象气质俱佳，统一黑金LOGO衬衫，享受尊贵服务。</span
              >
            </div>
            <div
              class="server-content animate__animated animate__fadeInUp animate__delay-2s"
              style="transition-delay: 0.4s"
            >
              <img src="../images/clothing.10b90e5d.png" />
              <p class="server-name">服装</p>
              <p class="font-style">Dress</p>
              <span
                >选用高端统一定制服装，尺码齐全，服装定期送洗，高频率更新更换，保证服装质感。</span
              >
            </div>
            <div
              class="server-content animate__animated animate__fadeInUp animate__delay-3s"
              style="transition-delay: 0.6s"
            >
              <img src="../images/makeup.96d6b5c7.png" />
              <p class="server-name">化妆</p>
              <p class="font-style">Makeup</p>
              <span
                >配备一线大牌化妆品、热门化妆单品，迪奥、香奈儿、雅诗兰黛、阿玛尼等一次性化妆用具，确保干净专一。</span
              >
            </div>
            <div
              class="server-content animate__animated animate__fadeInUp animate__delay-4s"
              style="transition-delay: 0.8s"
            >
              <img src="../images/space.c42043e6.png" />
              <p class="server-name">空间</p>
              <p class="font-style">Space</p>
              <span
                >刷新视觉嗅觉，顶级音响烘托，全套BOSE室内音响系统，airaroma室内香氛系统，专属海马体独有味道。</span
              >
            </div>
          </section>
        </div>
      </div>
    </div>
    <!-- 关于我们 -->
    <div class="padding about-us">
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
        <p>
          这里是毛衫与白摄影工作室,期待与您的合作! #街拍美女 #街头潮范儿
          #人像摄影 #校园 #德州学院
        </p>
      </div>
      <div class="content-cell pos-img">
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img
            @click="
              {
              }
            "
            src="../images/抖音.png"
            class="code-icon"
          />
          <!-- </a> -->
          <!-- <div class="code douyin" ref="douyin">
            <img src="../images/douyin-code.png" alt="">
            <p class="code-attention">关注抖音</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/bilibili.png" class="code-icon" />
          <!-- </a> -->
          <!-- <div class="code bilibili" ref="bilibili"><img src="../images/bilibili-code.png" alt="">
            <p class="code-attention">关注b站</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/小红书.png" class="code-icon" />
          <!-- </a> -->
          <!-- <div class="code redbook" ref="addShow"><img src="../images/red-book-code.png" alt="">
            <p class="code-attention">关注小红书</p>
          </div> -->
        </div>
        <div class="code-content">
          <!-- <a href="#javascript;"> -->
          <img src="../images/公众号.png" class="code-icon" />
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
        <div class="company-logo">
          <img id="theImage" src="../images/毛衫与白LOGO.png" alt="" />
        </div>
        <div class="whiteplace"></div>
        <div class="company-content">
          <div class="content">
            <div class="title">联系海马体</div>
            <p>400-068-5666</p>
            <div class="content-cell pos-img" >
              <div class="code-content content0"  @mouseleave="
                    (event) => {
                      onLeave(event);
                    }
                  "
                  @mouseenter ="
                    (event) => {
                      onHover(event);
                    }
                  ">
                <img
               
                  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADoAAAA6CAMAAADWZboaAAAA51BMVEUAAADy8vXz8/by8vX////y8vby8vXy8vXy8vby8vXy8vXy8vXy8vb09Pfz8/by8vb19fX4+Pj39/f09P/////y8vUWFhrw8PPKysxxcXREREfp6ey/v8J7e38zMzaWlpmDg4cpKS0fHyMbGx+8vL+3t7qurrKjo6ebm5+RkZU7Oz8lJSnv7/Ls7O+IiItAQETk5Off3+Ha2t3NzdCYmJuMjI9ra29iYmVZWV1JSU02Njrh4eTQ0NPFxcmoqKygoKN3d3pdXWFWVlouLjLj4+bV1dnBwcSXl5qAgIRSUlXm5unc3N9QUFTaB/k7AAAAFXRSTlMA9sadBnb57OPfuKd7YFY9MyUgGAxR0/NQAAAC1UlEQVRIx6WXaVviMBDHe3ALouJMS2kpbbkPRRRFvMX12N3v/3k2aeg2Pbie/N5o5sk/kyEzyVRKJVPNqkoxn8vli4qarWakPTmvlGSIIJcq53sIT9VQx6vV0x3CsyPYyNHZFmGmLMMW5PLGoGsK7ECppStPCrCTwkma8liGPZCPk8os7Ek24RP2Jub3RN5fKkfirRXgAAo17jwVOAglPN8yHEj5f/bJh0rlICePts/76N4M+u1JNJ/XtbJdeeUgxa3/4q2sjtTt0kdc49qcVfUre1ek7b6u925dIm5x0dLar6T76rfsh8i+74i2G44rRFpK6rSegYRmY+321Xoh/9aJRYOAEkmH5H51Axk3bHyJiI4O4yGiGe44I1UTymcX11jMMOuYdRwCzBEvwmnVZLG1mIx5nfZe7xatKYCB12AiWlzxJY7mFkPu3z2kDMfEbIIekapSLPPrmMYnsT9BF7HP1YBUjCgvMBUdHjr+sno4tSjleWUnmNtc1K3bt79LNloG6zpaODcv5ThlY4WUS/tPYJkNmnSh3m9/9DSDkFxE2vIddtky63wY+0b3BeLk+A1rtEZ+pjR/FiPElcXUA6R8x6V5qRiN9JJOf0WGwYqUJddjTFqUlOh+2+RvDwPm3M9ux6SKpEbO1AlyFr3OPXHr27+Q8hWTqnwi2mxuA3HwoS/nJNwmlyZP8VeAT/9rxJFGKhN/yMBCwjs1T10/GSFGNVJ0ZIvPANpoOIFZEwkdaqU1HpZbWHSRUtc9dMjldYOO4dFwn+mJse1eQIxS7ILperhqk1N6dxFH9WsaxD1SBhCnEr/WzCXim6nB+KGhEY/mnefH+ZlQyueJy3QyJ0E6b99237YWI5bSvTEkUNOucK1tGS6u8YyWDmmcbnw4rswXe9Dv6pNNjZDAcyXwSAo8zQINgUAbItD8CLRcAo2eQHsp0NQKtNICDbzAZ4PYx4rAJ9I/XFXswQ0ndH8AAAAASUVORK5CYII="
                  class="code-icon"
                />
                <div class="code">
                  <img src="http://www.haimati.cn/img/weibo-code.58a3a435.png" alt="" />
                  <p class="code-attention">关注微博</p>
                </div>
              </div>
              <div class="code-content content1" @mouseleave="
                    (event) => {
                      onLeave(event);
                    }
                  "
                  @mouseenter ="
                    (event) => {
                      onHover(event);
                    }
                  ">
                <img
                
                  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADoAAAA6CAMAAADWZboaAAAA8FBMVEUAAADy8vXy8vXz8/by8vX////y8vXy8vXy8vby8vXy8vXy8vXy8vby8vb09Pfz8/b19fX4+Pj39/f09P/////y8vby8vby8vby8vUWFhpQUFQZGR2rq65kZGjw8PN3d3rq6u0iIiYgICPl5ejh4eTe3uG3t7ouLjIpKS6Li457e39tbXE9PUHs7O/a2t3Kys27u75cXGAcHCCwsLOioqafn6KDg4d8fIBpaW1UVFhISEw0NDjW1trS0tXExMjBwcSXl5qSkpaAgIRzc3ZGRkklJSnQ0NO9vcClpalaWl1BQUU/P0QnJyvU1NekpKhcXF9nHZotAAAAGHRSTlMA9vXGnQb57OPfuKd7dmBWMyUgGAw+dz1gvz7aAAACmElEQVRIx6WX6ULiMBSFKS374oLoOVZqW3YQGEDBfd91Zt7/bSYlqaKiQOb7FWi+NttNbiIziW3lLDOViMcTKdPKbcUiC7KRT0fxgWg6v7GAuGYp75Ntrc0R1zP4lsz6D2Isa+AHjOy3nS6YmINZmG2uJjGX5Oosc8XAAhgrX81NLMjml29iYVY+9dPAwhgf+ltIYgmShan5NLEU5vv8ZrEk2bfVZ2BJjHBNZrA0GRUr0EDGkQUNrElkR6FBNIj9PLTICzUNLdJiOUShRTQWKWKKoe/3obiy2YLjup1OxwEc59bzah0IXEwoRnKYYofchsRtcFDFPic8YpsB9u05rnmNgFzE+ka9JNvAgVRHOKKkcW/zTk2PCUW5UlGqKMA5of3bre5IYR8tKv54/kjGQCQFyQPZkKr40u6kpTb9SrUk/uoCqNbFG8SPseNIIRVJQCKEF6k+kn9xzIAWsEuWEHBCDq+D54pEJA5JkzySao28RYmCQTVUH24OfVFB6F7zTApxpcoqUu2RdcAdkzcI1W2+MxgqNWxwSfRQql3SduC+0u7OVPmsGpyCRDxsStUlWQ0m5/XwIlRro1FDFMat1jPpqWEygXAUalKFqHQ+GSevHKqCPfIXEHTHVpNjQVIny0p9InsYe0EzvqpnoWq9LcQmj6HUS1Gs1M4vzhx0u4fk0+mp86aekgO1EIuQlO92yv0Xsg+49SH6JP2q8CRXSt3tH1EtxK33oKvBachKuECPgtY9Q5pKvaGgpIJuOtRre412BwFt3/fqlbYdchBMwaCHcrteb5dVqOtvMPrbmv5m+r9buP7BoX9c6R+S+kezfkKgn4boJz/6KZd+oqefXuontfqptH4Cr39t0L+szCdWnL4iFWd38R881AqyxRuRGwAAAABJRU5ErkJggg=="
                  class="code-icon "
                />
                <div class="code">
                  <img src="http://www.haimati.cn/img/red-book-code.e0e894f3.png" alt="" />
                  <p class="code-attention">关注小红书</p>
                </div>
              </div>
              <div class="code-content content2"  @mouseleave="
                    (event) => {
                      onLeave(event);
                    }
                  "
                  @mouseenter ="
                    (event) => {
                      onHover(event);
                    }
                  ">
                <img
               
                  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADoAAAA6CAMAAADWZboaAAAAzFBMVEUAAADy8vXy8vX////y8vXy8vXy8vXy8vby8vXy8vbz8/Xy8vXy8vXy8vby8vb09Pfz8/b19fX4+Pj39/f09P/////y8vby8vby8vby8vUAAACurrAICAg3NzcFBQULCwvg4ONBQULp6eyDg4V9fX5vb3Dt7fCwsLKpqauJiYtsbG1KSks8PD0eHh7d3d/W1tm+vsG2trixsbOoqKqRkZJ0dHZSUlMxMTErKywjIyMUFBUSEhPu7vHj4+bT09bGxsirq62fn6FEREUzMzOKpeTWAAAAGXRSTlMA9p0G/vns49/HxLine3ZgVjMlIBgMPnc9HbEJEAAAAf1JREFUSMell+l6ojAUhhNARECwbvVkBPdOtdpl2uk6+9z/PRV5Ugs9BxLT9x8/3if5OFlOGIk9iizfcxsN1/OtaGQzTQZxwKEED+KBhti1OBBwq6sQe6EDFThhr0a02xxq4O3K0P0WKGj1afOkCUqaJ5TZ4aAB72DzFDQ5RWOCNp0PObm+ykt5+004gma/UM8WHEXrvb5tOJL2YfVVBv0mMp6JuD2phlCriktAhHKvOJXq11xdA8Lp5qoFCvXxByCsfGdzlSq+E2n3ez+Gar4I6eJMcaYGGqpIbudQJmDM5gpVku4+zNhmQ1CqEigzZJGpGjFLqU7WE0q1mE8pV8vkeXz/psJ08YhVn3lYPNuke+XfQc34eX0OZTzmIvMyETmzg0risgYaU5oHdUyrDayuhKaKJjwd597/u5ubetVFv2mZm0vnvTgprXqoODORcQGgVH20JHYi41xDtdBCzKP+lh9/arJGaPk/FUddi4wnWh2hTbctZHUeRMY9aXIbbfWF2LMolPiOVAN5wOC6Xtxe/92KPS9zUo2JY20lyizo+Q6Iw/TsoWRuHbo05BE+TQpmMiVNp0tfHPNNKsV0MweSsPK6+rVMdpOX2eoKaHjP/JL83NVs3hCYtyHmzY95y2Xe6Jm3l+ZNrXkrbd7Amz8bzB8rauxh8Yk0pCO+Aj4vBeM6I23yAAAAAElFTkSuQmCC"
                  class="code-icon"
                />
                <div class="code">
                  <img src="http://www.haimati.cn/img/douyin-code.f8cf25d2.png" alt="" />
                  <p class="code-attention">关注抖音</p>
                </div>
              </div>
            </div>
          </div>
          <div class="company-code">
            <img src="../images/review-code.png" alt="" />
            <p>扫码预约拍摄</p>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>浙公网安备 33011802000662</p>
        <p>
          <a href="https://beian.miit.gov.cn/" target="_blank" class="jump-page"
            >浙ICP备11062584号-3</a
          >
        </p>
      </div>
    </div>
  </div>
</template>
<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
import "../../public/css/swiper.min.css";
import image0 from "../images/banner1.jpg";
import image1 from "../images/banner1.jpg";
import image2 from "../images/banner1.jpg";
export default {
  name: "Home",
  components: {
    swiper,
    swiperSlide,
  },
  data() {
    return {
      list: [1, 2, 3, 4],
      image0,
      image1,
      image2,
      arr: ["精致证件照", "职业形象照", "文艺照", "花颜照", "轻婚纱"],
      isShow: true,
      swiperOption: {
        loop: true,
        // 显示分页
        pagination: {
          el: ".swiper-pagination",
          clickable: true, //允许分页点击跳转,
          bulletElement: "span",
        },
        // 设置点击箭头
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
      idListener: ["id111", "newproduct"],
    };
  },
  // computed: {
  //   swiper() {
  //     return this.$refs.mySwiper.swiper;
  //   }
  // },
  mounted() {
    // 然后你就可以使用当前上下文内的swiper对象去做你想做的事了
    console.log("this is current swiper instance object", this.swiper);
    window.addEventListener("scroll", this.scroll);
    (function invert() {
      document.getElementById("theImage").style.filter = "invert(100%)";
    })();
  },
  methods: {
    handleTab(val) {
      this.isShow = val;
    },
    scroll() {
      this.scrollToTop();
      this.newestToTop();
    },
    scrollToTop() {
      // 获取视窗高度
      var domHight = document.body.offsetHeight;
      // dom滚动位置
      var scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
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
            ele.className =
              "process-content animate__animated animate__fadeInUp";
          } else {
            ele.className = `process-content animate__delay-${
              i - 1
            }s animate__animated animate__fadeInUp`;
          }
          // console.log('元素出现在可视区');
        } else {
          // console.log('元素不在可视区');
        }
      });
    },
    newestToTop() {
      // 获取视窗高度
      var domHight = document.body.offsetHeight;
      // dom滚动位置
      var scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      // 获取监听元素
      var newest;
      // 获取监听元素本身高度
      var scrollHeight;
      // 获取监听元素距离视窗顶部距离
      var offsetTop;
      // 获取监听元素距离顶部高度-窗口高度
      var top;
      // 元素距离底部的高度+元素本身高度
      var bottom;
      this.idListener.forEach((element) => {
        let ele = document.getElementById(element);
        scrollHeight = ele.scrollHeight;
        offsetTop = ele.offsetTop;
        top = offsetTop - domHight > 0 ? offsetTop - domHight : 0;
        bottom = scrollHeight + offsetTop;
        // 页面滚动位置 > 元素距离顶部高度-窗口高度 && 页面滚动位置 < 元素距离顶部高度+元素本身高度
        if (scrollTop >= top && scrollTop <= bottom) {
          console.log("元素不在可视区", ele.id);
        } else {
          ele.classList.add("animate__animated", "animate__fadeInUp");
          console.log(scrollTop, top);
          console.log("元素出现在可视区", ele.id);
        }
      });
    },
    onHover(e) {
      var code =e.srcElement.getElementsByClassName('code')[0];
      code.style.zIndex=0;
      code.style.opacity=1;
      // console.log(e.srcElement);
    },
    onLeave(e) {
      var leave =e.fromElement.getElementsByClassName('code')[0];
      leave.style.zIndex=-1;
      leave.style.opacity=0;
      console.log(e);
    }
  },
};
</script>

<style >
.btn1:hover {
  background-color: #000;
  color: #fff;
  transition-duration: 0.8s;
}

.btn2:hover {
  background-color: #c5a563;
  color: #fff;
  transition-duration: 0.8s;
}

.padding {
  /* margin: 0 ; */
  padding: 80px 10%;
}

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
  transition: opacity 0.05s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.item-title {
  background: center no-repeat;
}

.main .el-carousel__item {
  background-position: center top;
}

.main .el-carousel__item:nth-of-type(1) {
  background-image: url(../images/banner1.jpg);
}

.main .el-carousel__item:nth-of-type(2) {
  background-image: url(../images/banner2.jpg);
}

.main .el-carousel__item:nth-of-type(3) {
  background-image: url(../images/banner3.jpg);
}

.main .el-carousel__container .el-carousel__arrow {
  background-color: rgba(135, 135, 135, 0.15);
  width: 6%;
  height: 10%;
  top: 95%;
}

.main .el-carousel__arrow i {
  font-size: 30px;
  font-weight: 600;
  color: rgb(34, 34, 34);
}

.main .el-carousel__container .el-carousel__arrow--left {
  border-radius: 5px 0 0 5px;
  left: 44%;
}

.main .el-carousel__container .el-carousel__arrow:hover {
  background-color: rgba(135, 135, 135, 0.4);
}

.main .el-carousel__container .el-carousel__arrow--right {
  border-radius: 0 5px 5px 0;
  right: 44%;
}

/* 最新产品 */
.new-product {
  overflow: visible !important;
}

.new-product-wrap {
  /* padding: 90px 0 20px; */
}

.new-product-wrap .block {
  position: relative;
  width: 80%;
  margin-top: 80px;
}

.new-product-wrap .el-carousel {
  transition-delay: 0.6s;
  width: 70%;
  text-align: center;
  /* margin: 80px auto 0; */
}

.new-product-wrap .el-carousel__container {
  position: relative;
}

.new-product-wrap .el-carousel .el-carousel__arrow {
  position: absolute;
  font-size: 80px;
  color: gray;
  top: 30%;
  background-color: transparent;
}

.new-product-wrap .el-carousel .el-carousel__arrow {
  position: absolute;
  font-size: 80px;
  color: gray;
  top: 30%;
}

.new-product-wrap .el-carousel .el-carousel__arrow--left {
  left: -80px;
  z-index: 9999;
}

.new-product-wrap .el-carousel .el-carousel__arrow--right {
  z-index: 9999;
  right: -40px;
}

.new-product-wrap .el-carousel .el-carousel__indicators {
  position: absolute;
  height: 6%;
  top: -60px;
  background-color: transparent;
}

.new-product-wrap
  .el-carousel
  .el-carousel__indicator
  .el-carousel__button
  span {
  font-size: 20px;
}

.el-carousel__indicator {
  width: 15%;
}

.new-product .el-carousel__indicator:nth-child(-n + 4) {
  height: 20px;
  text-align: center;
  padding: 0;
  border-right: 1px solid #000;
  width: 15%;
}

.new-product .el-carousel__button {
  color: #232323 !important;
  width: 100%;
  padding: 0;
}

.new-product-wrap .el-carousel__item img {
  width: 100%;
  cursor: pointer;
}

.new-product-wrap .el-carousel__item .title {
  cursor: pointer;
  padding: 50px 0 8px;
  color: #333;
  font-size: 24px;
  font-weight: 600;
}

.new-product-wrap .el-carousel__item .tip {
  cursor: pointer;
  padding-bottom: 50px;
  color: #919199;
  font-size: 14px;
  font-weight: 400;
}

.new-product-wrap .el-carousel__item .detail-btn {
  width: 368px;
  height: 52px;
  line-height: 52px;
  margin: 0 auto 80px;
  color: #000;
  font-size: 14px;
  border: 1.5px solid #000;
  border-radius: 26px;
  cursor: pointer;
}

.newest {
  height: 840px;
  top: 80px;
}

.el-carousel__indicators--outside button {
  background-color: transparent;
}

.newnewest {
  width: 50%;
  margin: 0 auto;
}

.product-banner-container .carousel-img {
  width: 938px;
  font-size: 0;
}

.product-banner-container .carousel-img img {
  width: 100%;
}

.product-banner-container .carousel-img img {
  cursor: pointer;
}

.title {
  cursor: pointer;
  padding: 10px 0 8px;
  color: #333;
  font-size: 24px;
  font-weight: 600;
}

.product-banner-container .carousel-img .tip {
  cursor: pointer;
  padding-bottom: 50px;
  color: #919199;
  font-size: 14px;
  font-weight: 400;
}

.product-banner-container .carousel-img .detail-btn {
  width: 368px;
  height: 52px;
  line-height: 52px;
  margin: 0 auto 80px;
  color: #000;
  font-size: 14px;
  border: 1.5px solid #000;
  border-radius: 26px;
  cursor: pointer;
}

.product-banner-container .carousel-img .detail-btn p,
.product-banner-container .carousel-img .detail-btn span {
  display: inline-block;
}

.lazy-animate-init.lazy-animate-run {
  -webkit-transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: transform 0.5s ease, opacity 0.5s linear;
  transition: transform 0.5s ease, opacity 0.5s linear,
    -webkit-transform 0.5s ease;
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

/* 关于我们 */

.about-us .line-wrap,
.standard-service-wrap .line-wrap,
.new-product-wrap .line-wrap,
.reservation-process-wrap .line-wrap {
  margin: 0 auto;
  position: relative;
}

.line-wrap .line,
.line-wrap .line-right {
  position: absolute;
  top: 45px;
  width: 25%;
  height: 1px;
  background-color: #ebebeb;
  display: inline-block;
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
  margin: -30px auto 0px;
  text-align: center;
}

.line-wrap .line-content .title {
  padding-bottom: 4px;
  color: #16161a;
  font-size: 24px;
  font-weight: 600;
}

.line-wrap .line-content p {
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

.line-wrap .line-content p:last-child {
  background-color: #000;
  margin-left: 4px;
}

/* 预约流程 */
.reservation-process-wrap {
  /* padding: 80px 0px; */
  background-color: #fafafa;
}

.reservation-process-wrap .process-wrap {
  /* width: 1152px; */
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

.reservation-process-wrap
  .process-wrap
  .process-content:not(:last-child)::after {
  position: absolute;
  content: "";
  width: 160px;
  height: 1px;
  background-color: #d8d8d8;
  top: 635px;
  right: -80px;
}

.reservation-process-wrap .process-wrap .process-content .item-width,
.reservation-process-wrap .process-wrap .process-content img {
  width: 100%;
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

.tab-wrap .tab-content .golden:last-child .server-name {
  color: #c5a563 !important;
}

.tab-wrap .tab-content .golden:last-child p {
  color: #f0e2c7 !important;
  font-weight: 400;
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
  margin: 60px 13% 0 13%;
}

.tab-wrap .tab-content .tab-section.active {
  display: block;
  -webkit-transition: all 2s;
  transition: all 2s;
}

.tab-wrap .tab-content .tab-section {
  margin: 0px auto;
  display: none;
}

.tab-wrap .tab-content .tab-section .server-content {
  display: inline-block;
  width: 18%;
  vertical-align: top;
  margin: 0 1%;
}

.lazy-animate-init.lazy-animate-run {
  -webkit-transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: transform 0.5s ease, opacity 0.5s linear;
  transition: transform 0.5s ease, opacity 0.5s linear,
    -webkit-transform 0.5s ease;
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
  width: 100%;
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
  color: #8b8b8b;
}

.tab-wrap .tab-content .tab-section .golden p {
  padding-bottom: 14px;
  font-size: 14px;
  font-family: IBMPlexSansBold;
  color: #dfcca6 !important;
}

.tab-wrap .tab-content .tab-section .server-content .font-style {
  font-style: oblique;
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
}

.about-us {
  background-color: #fafafa;
}

.about-us .title h1,
.about-us .introduction p {
  text-align: center;
  margin-bottom: 50px;
}

.lazy-animate-init.lazy-animate-run {
  -webkit-transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: opacity 0.5s linear, -webkit-transform 0.5s ease;
  transition: transform 0.5s ease, opacity 0.5s linear;
  transition: transform 0.5s ease, opacity 0.5s linear,
    -webkit-transform 0.5s ease;
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

.about-us .code-content {
  width: 50%;
  height: 80px;
}

.pos-img .code-content .code-icon {
  width: 150px;
}

.content-cell img {
  display: inline-block;
}

/* footer */
.footer-wrap {
  width: 100%;
  background-color: #fafafa;
  border-top: 1px solid #e3e3e6;
}

.footer-wrap .footer-content {
  display: flex;
  margin: 24px auto;
  width: 70%;
}

.footer-wrap .footer-content .company-logo {
  height: 120px;
  flex: 1;
}

.footer-wrap .footer-content .company-logo img {
  margin-top: -10% !important;
  line-height: 120px;
  width: 200px;
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

/* 小图标 */

.footer-wrap .footer-content .company-content .content .pos-img {
  /* position: absolute; */
  bottom: 21px;
}

.footer-wrap .footer-content .company-content .content .content-cell {
  display: table-cell;
  text-align: center;
  padding: 5px 58px;
  font-size: 12px;
  color: #919199;
  cursor: pointer;
}

.footer-wrap .footer-content .company-content .content .pos-img .code-content {
  position: relative;
  display: inline-block;
  padding: 0px 10px;
}

.footer-wrap
  .footer-content
  .company-content
  .content
  .pos-img
  .code-content
  .code-icon {
  width: 29px;
  height: 29px;
}

.footer-wrap .footer-content .company-content .content .content-cell img {
  display: inline-block;
}

.footer-wrap
  .footer-content
  .company-content
  .content
  .pos-img
  .code-content
  .code {
  position: absolute;
  width: 174px;
  height: 190px;
  background: url(data:image/png;base64,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);
  background-size: 100%;
  background-repeat: no-repeat;
  opacity: 0;
  top: -190px;
  left: -72px;
  z-index: -1;
}

.footer-wrap
  .footer-content
  .company-content
  .content
  .pos-img
  .code-content
  .code
  img {
  width: 140px;
  height: 140px;
  /* margin-left: 16px; */
  margin-top: 20px;
}

.footer-wrap .footer-content .company-content .content .content-cell img {
  display: inline-block;
}

.footer-wrap
  .footer-content
  .company-content
  .content
  .pos-img
  .code-content
  .code
  .code-attention {
  color: #16161a;
}

.footer-wrap
  .footer-content
  .company-content
  .content
  .pos-img
  .code-content
  .code
  p {
  text-align: center;
  margin-top: -2px;
}
</style>