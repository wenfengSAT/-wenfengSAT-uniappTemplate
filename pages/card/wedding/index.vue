<template>
  <div class="greeting-card-page">
    <greeting-card-comp
      :switchType="2"
      itemClass="greeting-card-item"
      partClass="greeting-card-part"
      :arrow="true"
      :partsAnimate="true"
      music-src="http://mp3.9ku.com/hot/2004/07-17/41813.mp3"
      :music-autoplay="true"
      @pageHide="pageHide"
      @pageShow="pageShow"
    >
      <!--  -->
      <div class="H5FullscreenPage-wrap">
        <!--  -->
        <div class="greeting-card-item item1">
          <!-- 金色 -->
          <div class="greeting-card-part rollInLeft shang_img">
            <img src="/static/wedding/2.png" alt="" />
          </div>
          <div class="greeting-card-part rollInRight shang_img shang_img_b">
            <img src="/static/wedding/21.png" alt="" />
          </div>
          <!-- 线条 -->
          <div
            class="greeting-card-part top_Xial slideUp"
            data-delay="400"
          ></div>
          <div
            class="greeting-card-part top_Xial top_Xial_b slideDown"
            data-delay="400"
          ></div>
          <!--hua  金花  -->
          <div
            class="greeting-card-part fadeIn jinse_hua"
            data-delay="1000"
          ></div>
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_x"
            data-delay="1000"
          ></div>
          <!-- 叶子 -->
          <div class="greeting-card-part slideLeft yezi_zuo"></div>
          <div class="greeting-card-part slideLeft yezi_zuo yezi_zuo_zq"></div>
          <div class="greeting-card-part slideDown yezi_zuo_xx"></div>
          <div class="greeting-card-part slideDown yezi_zuo_yrx"></div>
          <div class="greeting-card-part zoomIn piao_gif" data-delay="1500">
            <img src="/static/wedding/jingy.gif" alt="" />
          </div>
          <!-- 中间 -->
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="800">
            <img src="/static/wedding/19.png" alt="" />
          </div>
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="1000">
            <img class="nie" src="/static/wedding/19.png" alt="" />
          </div>
          <!-- 中间叶子 -->
          <div
            class="greeting-card-part fadeIn yezi_zhongk"
            data-delay="1300"
          ></div>
          <div
            class="greeting-card-part fadeIn yezi_zhongk_x"
            data-delay="1300"
          ></div>
          <!-- 字 -->
          <div class="greeting-card-part zhongjiek_Ge" data-delay="1800">
            <img src="/static/wedding/9.png" alt="" />
          </div>
          <div class="greeting-card-part zhongjiek_Ge" data-delay="1800">
            <img class="nio" src="/static/wedding/1.png" alt="" />
          </div>
          <!-- 文字 -->
          <div class="greeting-card-part xinniang_xinlang" data-delay="1800">
            <p>Mr.志明<b>&</b>春娇.Miss</p>
            <dd>2020/05/20</dd>
            <span
              >You two are the prince and princess in a fairy
              tale and may you live happily everafter!</span
            >
          </div>
          <!-- 修改 -->
          <!-- <div class="xiugai_nige"></div> -->

          <!--  -->
          <!-- <div class="greeting-card-part part1 fadeIn" data-delay="1000"> </div>
            <div class="greeting-card-part part2 fadeIn"></div> -->
        </div>
        <!--  -->
        <div class="greeting-card-item item2">
          <!-- 金色 -->
          <div class="greeting-card-part rollInLeft shang_img">
            <img src="/static/wedding/2.png" alt="" />
          </div>
          <div class="greeting-card-part rollInRight shang_img shang_img_b">
            <img src="/static/wedding/21.png" alt="" />
          </div>
          <!-- 线条 -->
          <div
            class="greeting-card-part top_Xial slideUp"
            data-delay="400"
          ></div>
          <div
            class="greeting-card-part top_Xial top_Xial_b slideDown"
            data-delay="400"
          ></div>
          <!--hua  金花  -->
          <div
            class="greeting-card-part fadeIn jinse_hua"
            data-delay="1000"
          ></div>
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_x"
            data-delay="1000"
          ></div>
          <!-- 叶子 -->
          <div class="greeting-card-part slideLeft yezi_zuo"></div>
          <div class="greeting-card-part slideLeft yezi_zuo yezi_zuo_zq"></div>
          <div class="greeting-card-part slideDown yezi_zuo_xx"></div>
          <div class="greeting-card-part slideDown yezi_zuo_yrx"></div>
          <div
            class="greeting-card-part zoomIn piao_gif"
            data-delay="1500"
            style="width: 100%; height: 100%; top: 0"
          >
            <img src="/static/wedding/jingy.gif" alt="" />
          </div>
          <!-- 中间 -->
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="800">
            <img src="/static/wedding/19.png" alt="" />
          </div>
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="1000">
            <img class="nie" src="/static/wedding/19.png" alt="" />
          </div>
          <!-- 中间叶子 -->
          <div
            class="greeting-card-part fadeIn yezi_zhongk"
            data-delay="1300"
          ></div>
          <div
            class="greeting-card-part fadeIn yezi_zhongk_x"
            data-delay="1300"
          ></div>
          <!-- 字 -->
          <div
            class="greeting-card-part zhongjiek_Ge rentx_kuang"
            data-delay="1800"
          >
            <div class="rentx">
              <img src="/static/wedding/xinlang1.jpg" alt="" />
            </div>
          </div>
          <!-- 文字 -->
          <div class="greeting-card-part xinniang_xinlang" data-delay="1800">
            <p>新郎：志明</p>
            <dd style="line-height: 040rpx; padding-top: 020rpx">
              要你拥有会长大的幸福<br />一天比一天像公主，梦都被满足
            </dd>
            <!-- <span>You two are the prince and princess in a fairy tale and may you live happily everafter!</span> -->
          </div>
          <!--  -->
          <!-- 修改 -->
          <div class="xiugai_nige" style="left: 030rpx; top: 580rpx"></div>
          <!--  -->
        </div>
        <!--  -->
        <div class="greeting-card-item item3">
          <!-- 金色 -->
          <div class="greeting-card-part rollInLeft shang_img">
            <img src="/static/wedding/2.png" alt="" />
          </div>
          <div class="greeting-card-part rollInRight shang_img shang_img_b">
            <img src="/static/wedding/21.png" alt="" />
          </div>
          <!-- 线条 -->
          <div
            class="greeting-card-part top_Xial slideUp"
            data-delay="400"
          ></div>
          <div
            class="greeting-card-part top_Xial top_Xial_b slideDown"
            data-delay="400"
          ></div>
          <!--hua  金花  -->
          <div
            class="greeting-card-part fadeIn jinse_hua"
            data-delay="1000"
          ></div>
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_x"
            data-delay="1000"
          ></div>
          <!-- 叶子 -->
          <div class="greeting-card-part slideLeft yezi_zuo"></div>
          <div class="greeting-card-part slideLeft yezi_zuo yezi_zuo_zq"></div>
          <div class="greeting-card-part slideDown yezi_zuo_xx"></div>
          <div class="greeting-card-part slideDown yezi_zuo_yrx"></div>
          <div
            class="greeting-card-part zoomIn piao_gif"
            data-delay="1500"
            style="width: 100%; height: 100%; top: 0"
          >
            <img src="/static/wedding/jingy.gif" alt="" />
          </div>
          <!-- 中间 -->
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="800">
            <img src="/static/wedding/19.png" alt="" />
          </div>
          <div class="greeting-card-part fadeIn kuang_nieg" data-delay="1000">
            <img class="nie" src="/static/wedding/19.png" alt="" />
          </div>
          <!-- 中间叶子 -->
          <div
            class="greeting-card-part fadeIn yezi_zhongk"
            data-delay="1300"
          ></div>
          <div
            class="greeting-card-part fadeIn yezi_zhongk_x"
            data-delay="1300"
          ></div>
          <!-- 字 -->
          <div
            class="greeting-card-part zhongjiek_Ge rentx_kuang"
            data-delay="1800"
          >
            <div class="rentx">
              <img src="/static/wedding/ninnaing.jpg" alt="" />
            </div>
          </div>
          <!-- 文字 -->
          <div class="greeting-card-part xinniang_xinlang" data-delay="1800">
            <p>新娘：春娇</p>
            <dd style="line-height: 040rpx; padding-top: 020rpx">
              全世界都知道，我不在乎付出多少<br />我想这是幸福的写照
            </dd>
            <!-- <span>You two are the prince and princess in a fairy tale and may you live happily everafter!</span> -->
          </div>
          <!--  -->
          <!-- 修改 -->
          <div class="xiugai_nige" style="left: 030rpx; top: 580rpx"></div>
          <!--  -->
        </div>
        <!--  -->
        <div class="greeting-card-item item4">
          <div class="greeting-card-part rollInLeft shang_img">
            <img src="/static/wedding/2.png" alt="" />
          </div>
          <div class="greeting-card-part rollInRight shang_img shang_img_b">
            <img src="/static/wedding/21.png" alt="" />
          </div>
          <!-- 线条 -->
          <div
            class="greeting-card-part top_Xial slideUp"
            data-delay="400"
          ></div>
          <div
            class="greeting-card-part top_Xial top_Xial_b slideDown"
            data-delay="400"
          ></div>
          <!--hua  金花  -->
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_no"
            data-delay="1000"
          ></div>
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_x jinse_hua_no"
            data-delay="1000"
          ></div>
          <!-- 叶子 -->
          <div class="greeting-card-part slideLeft yezi_zuo"></div>
          <div class="greeting-card-part slideLeft yezi_zuo yezi_zuo_zq"></div>
          <div class="greeting-card-part slideDown yezi_zuo_xx"></div>
          <div class="greeting-card-part slideDown yezi_zuo_yrx"></div>

          <!-- 中间叶子 -->
          <div
            class="greeting-card-part fadeIn yezi_zhongk yezi_zhongk_dier"
            data-delay="1300"
          ></div>

          <!-- h婚纱照 -->
          <div class="greeting-card-part nimen_img slideDown" data-delay="1800">
            <img src="/static/wedding/nin_gs.jpg" alt="" />
          </div>
          <!-- 文字 -->
          <div class="greeting-card-part xinniang_xinlang" data-delay="1800">
            <!-- <p>新娘：春娇</p> -->
            <dd style="line-height: 040rpx; padding-top: 020rpx">
              深爱之人藏心不挂嘴<br />久念之人在梦不在眼
            </dd>
            <!-- <span>You two are the prince and princess in a fairy tale and may you live happily everafter!</span> -->
          </div>
          <!-- 修改 -->
          <!-- <div class="xiugai_nige"></div> -->
          <!--  -->
          <!--  -->
        </div>
        <!--  -->
        <div class="greeting-card-item item5">
          <div class="greeting-card-part rollInLeft shang_img">
            <img src="/static/wedding/2.png" alt="" />
          </div>
          <div class="greeting-card-part rollInRight shang_img shang_img_b">
            <img src="/static/wedding/21.png" alt="" />
          </div>
          <!-- 线条 -->
          <div
            class="greeting-card-part top_Xial slideUp"
            data-delay="400"
          ></div>
          <div
            class="greeting-card-part top_Xial top_Xial_b slideDown"
            data-delay="400"
          ></div>
          <!--hua  金花  -->
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_no"
            data-delay="1000"
          ></div>
          <div
            class="greeting-card-part fadeIn jinse_hua jinse_hua_x jinse_hua_no"
            data-delay="1000"
          ></div>
          <!-- 叶子 -->
          <div class="greeting-card-part slideLeft yezi_zuo"></div>
          <div class="greeting-card-part slideLeft yezi_zuo yezi_zuo_zq"></div>
          <div class="greeting-card-part slideDown yezi_zuo_xx"></div>
          <div class="greeting-card-part slideDown yezi_zuo_yrx"></div>

          <!-- 中间叶子 -->
          <div
            class="greeting-card-part fadeIn yezi_zhongk yezi_zhongk_dier"
            data-delay="1300"
          ></div>
          <!-- 字 -->
          <div
            class="greeting-card-part zhongjiek_Ge zhongjiek_Ge_er"
            data-delay="1800"
          >
            <img src="/static/wedding/9.png" alt="" />
          </div>
          <div
            class="greeting-card-part zhongjiek_Ge zhongjiek_Ge_er"
            data-delay="1800"
          >
            <img class="nio" src="/static/wedding/1.png" alt="" />
          </div>
          <!-- h婚纱照 -->
          <div
            class="greeting-card-part nimen_img nimen_img_text slideDown"
            data-delay="1800"
          >
            <div class="hou_tupian">
              <p>在最好的年华</p>
              <p>相见</p>
              <p>在最美的时光里</p>
              <p>相爱</p>
              <p>沉浸在幸福中的我们将于</p>
              <p>2020年5月20日（星期六）12:00</p>
              <p>举办婚礼</p>
              <p>诚邀您和您的家人出席</p>
              <p>新郎：志明 & 新娘：春娇</p>
              <p>席设</p>
              <p>贵州省贵阳市南明区国际大酒店</p>
              <p>期待您的到来</p>
              <p class="an">
                <a href="tel:18275330710">联系新郎</a>
                <a href="tel:18275330710">联系新娘</a>
              </p>
            </div>
          </div>
          <!-- 修改 -->
          <!-- <div class="xiugai_nige"></div> -->
          <!--  -->
        </div>
        <!--  -->
      </div>
    </greeting-card-comp>
  </div>
</template>

<script>
import GreetingCardComp from "@/components/GreetingCardComp";

export default {
  name: "greeting-card-page",
  components: {
    GreetingCardComp,
  },
  props: {},
  computed: {},
  watch: {},
  data() {
    return {};
  },
  created() {},
  mounted() {},
  methods: {
    pageHide() {
      // console.log("page hide.");
    },
    pageShow() {
      // console.log("page show.");
    },
  },
};
</script>

<style lang="scss" scoped>
@keyframes rotate {
  0% {
    -webkit-transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@-webkit-keyframes rotate {
  0% {
    -webkit-transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
  }
}

.greeting-card-page {
  text-align: center;

  .item1 {
    background-color: #00abd8;
    background: url("/static/wedding/16.gif") no-repeat left top;
    background-size: 100% 100%;
  }

  .item2 {
    background-color: #00abd8;
    background: url("/static/wedding/16.gif") no-repeat left top;
    background-size: 100% 100%;
  }
  .item3 {
    background-color: #00abd8;
    background: url("/static/wedding/16.gif") no-repeat left top;
    background-size: 100% 100%;
  }
  .item4 {
    background-color: #00abd8;
    background: url("/static/wedding/16.gif") no-repeat left top;
    background-size: 100% 100%;
  }
  .item5 {
    background-color: #00abd8;
    background: url("/static/wedding/16.gif") no-repeat left top;
    background-size: 100% 100%;
  }
  .item6 {
    background-color: #0067a6;
  }

  .item1 .part1 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item1 .part2 {
    position: absolute;
    bottom: 100px;
    right: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item3 .part1 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item3 .part2 {
    position: absolute;
    bottom: 100px;
    right: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item2 .part1 {
    position: absolute;
    top: 100px;
    right: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item2 .part3 {
    position: absolute;
    bottom: 60px;
    left: 19%;
    text-align: center;
    width: 150px;
    height: 150px;
    background-color: rgb(116, 178, 9);
  }
  .item2 .part2 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item4 .part1 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 100px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item4 .part2 {
    position: absolute;
    bottom: 100px;
    right: 19%;
    text-align: center;
    width: 150px;
    height: 150px;
    background-color: rgb(116, 178, 9);
  }
  .item5 .part1 {
    position: absolute;
    bottom: 100px;
    right: 19%;
    text-align: center;
    width: 150px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item5 .part2 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 150px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }

  .item6 .part2 {
    position: absolute;
    top: 100px;
    left: 19%;
    text-align: center;
    width: 150px;
    height: 100px;
    background-color: rgb(116, 178, 9);
  }
  .item6 .part1 {
    position: absolute;
    bottom: 100px;
    left: 19%;
    text-align: center;
    width: 250px;
    height: 250px;
    background-color: rgb(116, 178, 9);
  }

  .shang_img {
    position: absolute;
    top: -400rpx;
    left: -300rpx;
    text-align: center;
    width: 800rpx;
    height: 800rpx;
    /* animation:heart 1s ease infinite; */
  }
  .shang_img img {
    animation: heart 2s ease infinite;
    width: 100%;
  }
  .shang_img_b {
    top: initial;
    left: initial;
    right: -300rpx;
    bottom: -450rpx;
  }

  @keyframes heart {
    0% {
      opacity: 0.1;
    }
    50% {
      opacity: 1;
    }
    100% {
      opacity: 0.1;
    }
  }
  .top_Xial {
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    height: 300rpx;
    background: url("/static/wedding/15.png") no-repeat center;
    background-size: 100%;
    z-index: 1;
  }

  .top_Xial_b {
    top: initial;
    bottom: 0;
    left: 0;
    height: 300rpx;
    background: url("/static/wedding/7.png") no-repeat center;
    background-size: 100%;
  }

  .jinse_hua {
    width: 300rpx;
    position: absolute;
    top: 030rpx;
    right: -100rpx;
    height: 300rpx;
    background: url("/static/wedding/5.png") no-repeat center;
    background-size: 100%;
    animation: rotate 10s linear infinite; /*开始动画后无限循环，用来控制rotate*/
    animation-direction: normal;
  }
  .jinse_hua_x {
    background: url("/static/wedding/5.png") no-repeat center;
    background-size: 100%;
    top: initial;
    left: -050rpx;
    right: initial;
    bottom: 020rpx;
    animation: rotate 10s linear infinite; /*开始动画后无限循环，用来控制rotate*/
    animation-direction: normal;
  }
  @keyframes jinse_hua {
    0% {
      transform: rotate(0);
    }
    50% {
      transform: rotate(200deg);
    }
    100% {
      transform: rotate(0);
    }
  }

  .yezi_zuo {
    width: 150rpx;
    position: absolute;
    top: 150rpx;
    left: -030rpx;
    height: 150rpx;
    background: url("/static/wedding/26_1.png") no-repeat center;
    background-size: 80%;
    -webkit-transition: all 0.3s ease-in-out 0s;
    -o-transition: all 0.3s ease-in-out 0s;
    transition: all 0.3s ease-in-out 0s;
  }

  .yezi_zuo_zq {
    width: 250rpx;
    position: absolute;
    top: 450rpx;
    left: -100rpx;
    height: 250rpx;
    background: url("/static/wedding/yef.png") no-repeat center;
    background-size: 47%;
  }

  .yezi_zuo_xx {
    width: 100rpx;
    position: absolute;
    bottom: 0;
    left: 200rpx;
    height: 100rpx;
    background: url("/static/wedding/27.png") no-repeat center;
    background-size: 100%;
  }

  .yezi_zuo_yrx {
    width: 200rpx;
    position: absolute;
    bottom: 0;
    right: -100rpx;
    height: 500rpx;
    background: url("/static/wedding/ye.png") no-repeat center;
    background-size: 100%;
  }

  .kuang_nieg {
    width: 400rpx;
    position: absolute;
    bottom: 0;
    right: 0;
    top: -250rpx;
    left: 0;
    margin: auto;
    height: 400rpx;
    /* background:#fff; */
    background-size: 100%;
  }

  .kuang_nieg img {
    width: 100%;
    animation: rotate 10s linear infinite; /*开始动画后无限循环，用来控制rotate*/
    animation-direction: normal;
  }

  .kuang_nieg img.nie {
    animation: rotate 4s linear infinite; /*开始动画后无限循环，用来控制rotate*/
    animation-direction: normal;
    opacity: 0.5;
  }

  .yezi_zhongk {
    width: 280rpx;
    position: absolute;
    bottom: 0;
    right: -200rpx;
    top: -300rpx;
    left: 0;
    margin: auto;
    height: 400rpx;
    background: url("/static/wedding/10.png") no-repeat;
    background-size: 100%;
  }

  .yezi_zhongk_x {
    width: 280rpx;
    position: absolute;
    bottom: 0;
    right: 0;
    top: -250rpx;
    left: -250rpx;
    margin: auto;
    height: 420rpx;
    background: url("/static/wedding/8.png") no-repeat;
    background-size: 100%;
  }
  .piao_gif {
    width: 400rpx;
    position: absolute;
    bottom: 0;
    right: 0;
    top: -250rpx;
    left: 0;
    margin: auto;
    overflow: hidden;
    height: 450rpx;
  }
  .piao_gif img {
    width: 100%;
  }

  .zhongjiek_Ge {
    width: 380rpx;
    position: absolute;
    bottom: 0;
    right: 0;
    top: -150rpx;
    left: 0;
    margin: auto;
    height: 350rpx;
    /* background:#fff; */
    background-size: 100%;
    animation: rdhre 2s ease;
  }
  @keyframes rdhre {
    0% {
      opacity: 0.1;
    }
    100% {
      opacity: 1;
    }
  }
  .zhongjiek_Ge img {
    width: 100%;
  }

  .zhongjiek_Ge img.nio {
    animation: nemgen 3s ease infinite;
  }

  @keyframes nemgen {
    0% {
      opacity: 0.3;
    }
    50% {
      opacity: 1;
    }
    100% {
      opacity: 0.3;
    }
  }

  .xinniang_xinlang {
    width: 80%;
    position: absolute;
    bottom: -450rpx;
    right: 0;
    top: 0;
    left: 0;
    margin: auto;
    height: 200rpx;
    /* background: #fff; */
    background-size: 100%;
    animation: rdhre 2s ease;
  }
  .xinniang_xinlang p {
    font-size: 038rpx;
    color: #a78b6e;
  }
  .xinniang_xinlang p b {
    padding: 0 010rpx;
  }
  .xinniang_xinlang span {
    display: block;
    width: 80%;
    text-align: center;
    font-size: 020rpx;
    margin: auto;
    padding-top: 010rpx;
    color: #a78b6e;
    opacity: 0.5;
  }

  .xinniang_xinlang dd {
    text-align: center;
    line-height: 055rpx;
    color: #a78b6e;
    font-size: 024rpx;
  }

  .xiugai_nige {
    position: absolute;
    width: 065rpx;
    height: 065rpx;
    background: url("/static/wedding/xiug.png") no-repeat;
    background-size: 100%;
    left: 020rpx;
    top: 690rpx;
    z-index: 99;
  }

  /* 1 */
  .tanchu_xx_web1 {
    position: fixed;
    width: 100%;
    height: 100%;
    z-index: 999;
    top: 0px;
    left: 0px;
    display: none;
  }
  .tanchu_xx_web1 .tcc_beij_x_web {
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
  }
  .tanchu_xx_web1 .kuang_li {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    z-index: 999;
    width: 80%;
    max-width: 640px;
    min-height: 40%;
    min-height: 100rpx;
    height: fit-content;
    padding: 0;
    border-radius: 8px;
    background: #fff;
    overflow: hidden;
  }
  .tanchu_xx_web1 .kuang_li .off {
    width: 050rpx;
    z-index: 999;
    height: 050rpx;
    background: url("/static/wedding/off.png") no-repeat center;
    background-size: 035rpx;
    position: absolute;
    top: 010rpx;
    right: 010rpx;
  }
  .tanchu_xx_web1 .img_bj {
    width: 100%;
  }
  .tanchu_xx_web1 .bt {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    width: 90%;
    margin: auto;
    color: #fff;
  }
  .tanchu_xx_web1 .bt h2 {
    font-size: 032rpx;
    padding-top: 030rpx;
    line-height: 045rpx;
  }
  .tanchu_xx_web1 .bdkuan {
    width: 90%;
    margin: auto;
    padding-bottom: 040rpx;
  }
  .tanchu_xx_web1 .bdkuan .nim {
    color: #ff5527;
    display: block;
    padding-left: 035rpx;
    font-size: 020rpx;
    line-height: 035rpx;
    position: relative;
  }
  .tanchu_xx_web1 .bdkuan .nim::after {
    display: block;
    // background: url("/static/wedding/baohu_cj.png") no-repeat center;
    background-size: 025rpx;
    width: 030rpx;
    height: 035rpx;
    position: absolute;
    left: 0;
    top: 0;
    content: "";
  }
  .tanchu_xx_web1 .bdkuan input {
    width: 96%;
    border: solid 1px #b4b4b4;
    outline: none;
    height: 050rpx;
    line-height: 050rpx;
    padding: 0 2%;
    border-radius: 3px;
    margin: 010rpx 0;
    line-height: 050rpx;
    -webkit-appearance: none;
  }
  .tanchu_xx_web1 .bdkuan button {
    outline: none;
    width: 100%;
    height: 065rpx;
    line-height: 065rpx;
    border: none;
    background: #a78b6e;
    box-shadow: 0 2px 10px #bddbfb;
    color: #fff;
    font-weight: 500;
    border-radius: 100px;
    margin-top: 030rpx;
  }
  .tanchu_xx_web1 .bdkuan {
    line-height: 0;
  }

  .tanchu_xx_web1 .bt h2 {
    padding-top: 030rpx;
  }

  .tanchu_xx_web1 .bdkuan button {
    box-shadow: 0 2px 10px #eaeaea;
  }

  .tanchu_xx_web1 .bdkuan input {
    border: solid 1px #e4d8b9;
  }

  .jinse_hua_no {
    animation: none;
  }

  .yezi_zhongk_dier {
    top: inherit;
    left: 0;
    margin: auto;
    right: inherit;
    bottom: -600rpx;
    background: url("/static/wedding/8_1.png") no-repeat;
    background-size: 100%;
    width: 480rpx;
    height: 460rpx;
  }

  .zhongjiek_Ge_er {
    top: -550rpx;
  }

  .niben_banc {
    position: fixed;
    right: 0;
    bottom: 0;
    width: 130rpx;
    z-index: 999;
  }

  .niben_banc a {
    font-size: 024rpx;
    display: block;
    text-decoration: none;
    height: 055rpx;
    background: rgba(167, 139, 110, 0.8);
    margin-bottom: 020rpx;
    line-height: 055rpx;
    color: #fff;
    border-top-left-radius: 100px;
    border-bottom-left-radius: 100px;
    padding: 0 010rpx;
  }

  .rentx {
    border-radius: 50%;
    width: 350rpx;
    height: 350rpx;
    overflow: hidden;
  }

  .rentx img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .rentx_kuang {
    top: -250rpx;
  }

  .nimen_img {
    width: 500rpx;
    position: absolute;
    bottom: 0;
    right: 0;
    top: -100rpx;
    left: 0;
    border: solid 1px #a78b6e;
    margin: auto;
    height: 320rpx;
    background: #f00;
    background-size: 100%;
    border-radius: 3px;
  }

  .nimen_img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .nimen_img_text {
    background: none;
    border: none;
    height: 550rpx;
    top: 100rpx;
    z-index: 99;
  }
  .nimen_img_text .hou_tupian {
    line-height: 040rpx;
    color: #a78b6e;
  }
  .nimen_img_text .hou_tupian .an {
    overflow: hidden;
    padding-top: 020rpx;
    height: 050rpx;
  }
  .nimen_img_text .hou_tupian .an a {
    text-decoration: none;
    background: #a78b6e;
    color: #fff;
    padding: 010rpx 020rpx;
    margin: 0 010rpx;
    border-radius: 3px;
  }
}
</style>
