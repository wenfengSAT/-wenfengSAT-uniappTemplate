<template>
  <div class="birthday-card-page">
    <greeting-card-comp
      :switchType="2"
      itemClass="greeting-card-item"
      partClass="greeting-card-part"
      :arrow="true"
      :partsAnimate="true"
      :repeatAnimate="true"
      music-src="http://mp3.9ku.com/hot/2004/07-17/41813.mp3"
      :music-autoplay="true"
      @pageHide="pageHide"
      @pageShow="pageShow"
    >
      <!-- 第一页 -->
      <div class="greeting-card-item item1">
        <!-- 气球背景 -->
        <div class="greeting-card-part horizontal-centering top-balloon-bg">
          <img class="slideUp" src="/static/birthday/FkMpjWWZq3GSXfYsNKmrW427hj3j.webp" />
        </div>
        <!-- 生日蛋糕 -->
        <div
          class="
            greeting-card-part
            horizontal-centering
            zIndex-1
            middle-cake-icon
          "
        >
          <img class="slideUp" src="/static/birthday/FpxfniWt6b9fdBXKpms3S6I5CUoQ.webp" />
        </div>
        <!-- 生日快乐文字图 -->
        <div
          class="
            greeting-card-part
            horizontal-centering
            zIndex-1
            middle-text-img
          "
        >
          <img class="slideUp" src="/static/birthday/FvgGv1vOOvfN0CFKo38zGxm0S1EB.webp" />
        </div>
        <!-- 祝福文字 -->
        <div
          class="greeting-card-part horizontal-centering zIndex-1 slideUp"
          style="
            position: absolute;
            top: 970rpx;
            color: rgb(214, 152, 40);
            text-align: center;
            font-size: 28rpx;
            line-height: 60rpx;
          "
        >
          <p>今天是你的生日，你显得更加美丽！</p>
          <p>明媚的阳光，湛蓝的天空，</p>
          <p>都在帮我把最美好的祝福送给你！</p>
        </div>
        <div
          class="greeting-card-part horizontal-centering zIndex-1 slideDown"
          style="
            position: absolute;
            top: 1160rpx;
            font-size: 28rpx;
            color: #000;
            letter-spacing: 24rpx;
          "
        >
          HAPPYBIRTHDAY
        </div>

        <!-- 气球背景 底部 -->
        <div
          class="
            greeting-card-part
            horizontal-centering
            zIndex-0
            bottom-balloon-bg
          "
        >
          <img
            class="slideDown-slow"
            src="/static/birthday/FkMpjWWZq3GSXfYsNKmrW427hj3j.webp"
          />
        </div>
      </div>
      <!-- 第二页 -->
      <div class="greeting-card-item item2">
        <!-- 气球背景 -->
        <div
          class="greeting-card-part horizontal-centering top-balloon-bg"
          style="top: -200rpx"
        >
          <img class="slideUp" src="/static/birthday/FkMpjWWZq3GSXfYsNKmrW427hj3j.webp" />
        </div>

        <!-- 生日蛋糕 -->
        <div class="greeting-card-part horizontal-centering zIndex-1">
          <img
            class="slideUp"
            src="/static/birthday/FpxfniWt6b9fdBXKpms3S6I5CUoQ.webp"
            style="position: absolute; top: 310rpx; left: 60rpx; width: 100rpx"
          />

          <img
            class="slideUp"
            src="/static/birthday/FpxfniWt6b9fdBXKpms3S6I5CUoQ.webp"
            style="position: absolute; top: 310rpx; right: 60rpx; width: 120rpx"
          />
        </div>
        <!-- 生日快乐文字图 -->
        <div
          class="greeting-card-part horizontal-centering zIndex-1"
          style="position: absolute; top: 340rpx; width: 500rpx"
        >
          <img class="slideUp" src="/static/birthday/FvgGv1vOOvfN0CFKo38zGxm0S1EB.webp" />
        </div>

        <!-- 姓名 -->
        <div
          class="greeting-card-part horizontal-centering zIndex-1 slideUp"
          style="
            position: absolute;
            top: 550rpx;
            color: #000;
            text-align: center;
            font-size: 32rpx;
            letter-spacing: 5rpx;
            font-family: Microsoft Yahei;
          "
        >
          韩梅梅 HANMEIMEI
        </div>

        <!-- 照片 -->
        <div
          class="
            greeting-card-part
            horizontal-centering
            zIndex-1
            photo-border
            slideUp
          "
          style="position: absolute; top: 610rpx; width: 460rpx; height: 280rpx"
        >
          <img
            src="/static/birthday/o_1c4ghr10g5o01tsusnhlg1jkjp.jpg"
            style="width: 110%; left: 5%; top: 5%"
          />
        </div>

        <!-- 祝福文字 -->
        <div
          class="greeting-card-part horizontal-centering zIndex-1 slideUp"
          style="
            position: absolute;
            top: 930rpx;
            color: #000;
            text-align: center;
            font-size: 28rpx;
            line-height: 60rpx;
          "
        >
          <p>拥有一份美好的友谊，</p>
          <p>如同拥有一份甜美的祝福，但愿我们的千万</p>
          <p>祝福，永远陪伴你左右。生日快乐!</p>
        </div>
        <div
          class="greeting-card-part horizontal-centering zIndex-1 slideDown"
          style="
            position: absolute;
            top: 1160rpx;
            font-size: 28rpx;
            color: #000;
            letter-spacing: 24rpx;
          "
        >
          HAPPYBIRTHDAY
        </div>

        <!-- 气球背景 底部 -->
        <div
          class="
            greeting-card-part
            horizontal-centering
            zIndex-0
            bottom-balloon-bg
          "
        >
          <img
            class="slideDown-slow"
            src="/static/birthday/FkMpjWWZq3GSXfYsNKmrW427hj3j.webp"
          />
        </div>
      </div>
    </greeting-card-comp>
  </div>
</template>

<script>
import GreetingCardComp from "@/components/GreetingCardComp";

export default {
  name: "birthday-card-page",
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
.slideDown-slow {
  animation-name: slideDown-slow;
  animation-duration: 4s;
  animation-timing-function: ease-in-out;
}
@keyframes slideDown-slow {
  0% {
    opacity: 0;
    transform: translate3d(0, -50%, 0);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}

.birthday-card-page {
  text-align: center;

  // position: absolute;的水平居中类
  .horizontal-centering {
    left: 0;
    right: 0;
    margin: 0 auto;

    img {
      width: 100%;
    }
  }

  .zIndex-0 {
    z-index: 0;
  }
  .zIndex-1 {
    z-index: 1;
  }
  .zIndex-2 {
    z-index: 2;
  }

  .greeting-card-item {
    background: #fff;
  }

  .top-balloon-bg {
    position: absolute;
    top: -90rpx;
    left: -60rpx;
    width: 860rpx;
  }
  .bottom-balloon-bg {
    position: absolute;
    bottom: -440rpx;
    left: -60rpx;
    width: 860rpx;
  }

  .middle-cake-icon {
    position: absolute;
    top: 500rpx;
    width: 220rpx;
  }

  .middle-text-img {
    position: absolute;
    top: 730rpx;
    width: 610rpx;
  }

  .photo-border {
    border-width: 2px;
    border-style: solid;
    border-color: rgb(0, 0, 0);
    border-radius: 0px;
    overflow: hidden;
  }
}
</style>
