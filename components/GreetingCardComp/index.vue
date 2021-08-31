<template>
  <div class="greeting-card-comp">
    <slot></slot>

    <music-player
      :music-src="musicSrc"
      :music-autoplay="musicAutoplay"
    ></music-player>
  </div>
</template>

<script>
/**
 * 贺卡翻页与动画组件
 * 1）添加元素动画：首先设置partClass，如partClass=greeting-card-part。然后在元素上添加partClass以及动画执行的类rollInLeft，如
 *    <div class="greeting-card-part rollInLeft">
         <img src="./img/2.png" alt="" />
      </div>
 */

import musicPlayer from "./components/musicPlayer";

export default {
  name: "greeting-card-comp",
  components: { musicPlayer },
  props: {
    /**
     * 切页动画类型
     */
    switchType: {
      type: Number,
      default: 2,
    },
    /**
     * 每一页的class名。（注意！在<style>中的类名也要对应修改）
     */
    itemClass: {
      type: String,
      default: "greeting-card-item",
    },
    /**
     * 动画元素的的class名。（注意！在<style>中的类名也要对应修改）
     */
    partClass: {
      type: String,
      default: "greeting-card-part",
    },
    /**
     * 是否显示底部箭头
     */
    arrow: {
      type: Boolean,
      default: true,
    },
    /**
     * 翻页后页面元素动画是否重新执行
     */
    partsAnimate: {
      type: Boolean,
      default: true,
    },
    /**
     * 是否每次向前向后翻页都执行页面元素动画（默认只有第一次执行）
     */
    repeatAnimate: {
      type: Boolean,
      default: false,
    },
    /**
     * 音乐设置
     */
    "music-src": {
      type: String,
    },
    "music-autoplay": {
      type: Boolean,
      default: true,
    },
  },
  computed: {},
  watch: {},
  data() {
    return {
      switchAnimeObj: {
        1: {
          upDrag: function (percentage, itemObj) {
            var translateY = 1 - 0.7 * percentage; //位置系数，可以微调

            if (itemObj.nextItem) {
              //下一个item上移动
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0," + translateY * 100 + "%,0)";
            } else {
              itemObj.item.style["-webkit-transform"] =
                "translate3d(0," + -0.7 * percentage * 100 + "%,0)";
            }
          },
          downDrag: function (percentage, itemObj) {
            var translateY = -(0.7 * percentage);

            if (itemObj.prevItem) {
              //前一个item放大
              itemObj.prevItem.style["-webkit-transform"] =
                "translate3d(0," + (translateY * 100 - 100) + "%,0)";
            }

            //当前item下移动
            itemObj.item.style["-webkit-transform"] =
              "translate3d(0," + translateY * 100 + "%,0)";
          },
          nextSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "translate3d(0,-100%,0)";

            itemObj.nextItem.style["-webkit-transform"] = "translate3d(0,0,0)";
          },
          prevSlide: function (itemObj) {
            if (itemObj.prevItem) {
              itemObj.prevItem.style["-webkit-transform"] = "scale(1)";
            }
            itemObj.item.style["-webkit-transform"] = "translate3d(0,100%,0)";
          },
          showSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "scale(1)";
            if (itemObj.nextItem) {
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0,100%,0)";
            }
          },
        },
        2: {
          upDrag: function (percentage, itemObj) {
            let scale = 1 - 0.2 * percentage; //缩放系数，可以微调
            let translateY = 1 - 0.7 * percentage; //位置系数，可以微调

            //当前item缩小
            itemObj.item.style["-webkit-transform"] = "scale(" + scale + ")";

            if (itemObj.nextItem) {
              //下一个item上移动
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0," + translateY * 100 + "%,0)";
            }
          },
          downDrag: function (percentage, itemObj) {
            let scale = 0.8 - 0.2 * percentage;
            let translateY = -(0.7 * percentage);

            //当前item下移动
            itemObj.item.style["-webkit-transform"] =
              "translate3d(0," + translateY * 100 + "%,0)";
            if (itemObj.prevItem) {
              //前一个item放大
              itemObj.prevItem.style["-webkit-transform"] =
                "scale(" + scale + ")";
            }
          },
          nextSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "scale(.8)";

            itemObj.nextItem.style["-webkit-transform"] = "translate3d(0,0,0)";
          },
          prevSlide: function (itemObj) {
            if (itemObj.prevItem) {
              itemObj.prevItem.style["-webkit-transform"] = "scale(1)";
            }
            itemObj.item.style["-webkit-transform"] = "translate3d(0,100%,0)";
          },
          showSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "scale(1)";
            if (itemObj.nextItem) {
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0,100%,0)";
            }
          },
        },
        3: {
          upDrag: function (percentage, itemObj) {
            var translateY = 1 - 0.4 * percentage; //位置系数，可以微调
            itemObj.item.style["-webkit-transform"] =
              "translate3d(0," + (translateY * 100 - 100) + "%,0)";

            if (itemObj.nextItem) {
              //下一个item上移动
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0," + translateY * 100 + "%,0)";
            }
          },
          downDrag: function (percentage, itemObj) {
            var translateY = -(0.4 * percentage);
            if (itemObj.prevItem) {
              itemObj.prevItem.style["-webkit-transform"] =
                "translate3d(0," + (translateY * 100 - 100) + "%,0)";
            }

            //当前item下移动
            itemObj.item.style["-webkit-transform"] =
              "translate3d(0," + translateY * 100 + "%,0)";
          },
          nextSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "translate3d(0,-100%,0)";
            if (itemObj.nextItem) {
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0,0,0)";
            }
          },
          prevSlide: function (itemObj) {
            if (itemObj.prevItem) {
              itemObj.prevItem.style["-webkit-transform"] = "scale(1)";
            }
            itemObj.item.style["-webkit-transform"] = "translate3d(0,100%,0)";
          },
          showSlide: function (itemObj) {
            itemObj.item.style["-webkit-transform"] = "scale(1)";
            if (itemObj.nextItem) {
              itemObj.nextItem.style["-webkit-transform"] =
                "translate3d(0,100%,0)";
            }
          },
        },
      },
      itemList: [],
      dragThreshold: 0.15, //临界值
      dragStart: null, //开始抓取标志位
      percentage: 0, //拖动量的百分比
      currentItem: undefined,
    };
  },
  created() {},
  mounted() {
    this.init();
  },
  methods: {
    init() {
      let itemList = document.querySelectorAll(
        `.greeting-card-comp .${this.itemClass}`
      );
      if (!itemList || !itemList.length) {
        console.log("没有item");
        return;
      }

      this.itemList = itemList;
      this.currentItem = itemList[0];
      this.currentItem.setAttribute("state", "current");

      itemList.forEach((v) => {
        v.addEventListener("touchstart", this.onTouchstart, false, {
          passive: false,
        });
        v.addEventListener("touchmove", this.onTouchmove, false, {
          passive: false,
        });
        v.addEventListener("touchend", this.onTouchend, false);

        v.addEventListener(
          "transitionend",
          (event) => {
            if (event.target.getAttribute("state") === "current") {
              // 下一页显示，动画结束（不包括parts的动画）
              this.$emit("pageShow");
            } else {
              // 上一页隐藏，动画结束（不包括parts的动画）
              this.$emit("pageHide");
            }
          },
          false
        );
      });

      if (this.arrow) {
        this.itemList.forEach((v) => {
          let spanNode = document.createElement("span");
          spanNode.setAttribute("class", "item-down-arrow");
          v.appendChild(spanNode);
        });
      }

      if (this.partsAnimate) {
        this.itemList.forEach((item) => {
          item.querySelectorAll(`.${this.partClass}`).forEach((v) => {
            v.classList.add("hide");
          });
        });
        this.orderPart(this.itemList[0]);
      }
    },
    /**
     * 触摸事件方法
     */
    onTouchstart(event) {
      if (this.dragStart !== null) return;

      let item = event.target.closest(`.${this.itemClass}`);

      // console.log("item: ", item);

      if (!item) {
        console.log("item empty: ", item);
        return;
      }

      if (event.touches) {
        event = event.touches[0];
      }
      //抓取时的所在位置
      this.dragStart = event.clientY;

      //分别关闭item的动画效果,动画效果只在松开抓取时出现
      let { nextItem, prevItem } = this.findSiblings(item);
      item.classList.add("no-animation");
      if (nextItem) {
        nextItem.classList.add("no-animation");
      }
      if (prevItem) {
        prevItem.classList.add("no-animation");
      }
    },
    onTouchmove(event) {
      //防止ios拖动事件
      event.preventDefault();

      if (this.dragStart === null) return;

      let item = event.target.closest(`.${this.itemClass}`);

      // console.log("item: ", item);

      if (!item) {
        console.log("item empty: ", item);
        return;
      }

      if (event.touches) {
        event = event.touches[0];
      }

      //得到抓取开始时于进行中的差值的百分比
      this.percentage = (this.dragStart - event.clientY) / window.screen.height; //

      let { nextItem, prevItem } = this.findSiblings(item);
      if (this.percentage > 0) {
        // 向上拖动

        this.switchAnimeObj[this.switchType].upDrag(this.percentage, {
          item,
          prevItem,
          nextItem,
        });
      } else {
        //向下拖动

        this.switchAnimeObj[this.switchType].downDrag(this.percentage, {
          item,
          prevItem,
          nextItem,
        });
      }
    },
    onTouchend(event) {
      //防止多次滚动，故增加一个覆盖层
      // $(".overlay").show();
      this.dragStart = null;

      let item = event.target.closest(`.${this.itemClass}`);

      if (!item) {
        console.log("item empty: ", item);
        return;
      }

      let { nextItem, prevItem } = this.findSiblings(item);
      item.classList.remove("no-animation");
      if (nextItem) {
        nextItem.classList.remove("no-animation");
      }
      if (prevItem) {
        prevItem.classList.remove("no-animation");
      }

      //抓取停止后，根据临界值做相应判断
      if (this.percentage >= this.dragThreshold) {
        this.nextSlide({
          item,
          prevItem,
          nextItem,
        });
      } else if (Math.abs(this.percentage) >= this.dragThreshold) {
        this.prevSlide({
          item,
          prevItem,
          nextItem,
        });
      } else {
        this.showSlide({
          item,
          prevItem,
          nextItem,
        });
      }
      //重置percentage
      this.percentage = 0;
    },
    /**
     * 找到当前item的nextItem和prevItem
     */
    findSiblings(item) {
      let itemIndex;
      for (let i = 0, len = this.itemList.length; i < len; i++) {
        if (item === this.itemList[i]) {
          itemIndex = i;
        }
      }

      let nextItem, prevItem;

      if (itemIndex < this.itemList.length - 1) {
        nextItem = this.itemList[itemIndex + 1];
      }
      if (itemIndex > 0) {
        prevItem = this.itemList[itemIndex - 1];
      }

      // console.log("itemIndex: ", itemIndex);
      // console.log("nextItem, prevItem : ", nextItem, prevItem);

      return { nextItem, prevItem };
    },
    /**
     * 自动滑到下一张
     */
    nextSlide(itemObj) {
      //恢复到原样，或者展示下一item

      if (itemObj.nextItem) {
        // 在元素state上设置状态：前一个和当前显示的item
        this.itemList.forEach((v) => {
          v.removeAttribute("state");
        });
        itemObj.item.setAttribute("state", "prev");
        itemObj.nextItem.setAttribute("state", "current");

        if (this.repeatAnimate) {
          // 往后时重新执行页面元素动画
          itemObj.nextItem
            .querySelectorAll(`.${this.partClass}`)
            .forEach((v) => {
              v.classList.add("hide");
            });

          this.orderPart(itemObj.nextItem);
        } else {
          // 仅第一次往后翻页时执行
          this.orderPart(itemObj.nextItem);
        }

        this.currentItem = itemObj.nextItem;
        this.switchAnimeObj[this.switchType].nextSlide(itemObj);
      } else {
        this.switchAnimeObj[this.switchType].showSlide(itemObj);
      }
    },
    /**
     * 自动滑到上一张
     */
    prevSlide(itemObj) {
      if (itemObj.prevItem) {
        // 在元素state上设置状态：前一个和当前显示的item
        this.itemList.forEach((v) => {
          v.removeAttribute("state");
        });
        itemObj.item.setAttribute("state", "prev");
        itemObj.prevItem.setAttribute("state", "current");

        // 往前翻页时重新执行页面元素动画
        if (this.repeatAnimate) {
          itemObj.prevItem
            .querySelectorAll(`.${this.partClass}`)
            .forEach((v) => {
              v.classList.add("hide");
            });

          this.orderPart(itemObj.prevItem);
        }

        this.currentItem = itemObj.prevItem;
        this.switchAnimeObj[this.switchType].prevSlide(itemObj);
      } else {
        this.switchAnimeObj[this.switchType].showSlide(itemObj);
      }
    },
    showSlide(itemObj) {
      this.switchAnimeObj[this.switchType].showSlide(itemObj);
    },
    /**
     * 页面元素动画顺序执行
     */
    orderPart(dom) {
      let parts = dom.querySelectorAll(
        `.greeting-card-comp .${this.itemClass} .${this.partClass}`
      );
      // console.log("parts: ", parts);
      if (!parts || !parts.length) {
        console.log("没有parts");
        return;
      }

      parts.forEach(function (v) {
        let delay = v.getAttribute("data-delay") || 100;
        setTimeout(function () {
          v.classList.remove("hide");
        }, delay);
      });
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./page-animation.css";

.greeting-card-comp {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  position: relative;
  .greeting-card-item {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    transition: all 700ms cubic-bezier(0.55, 0.085, 0, 0.99);
    background-position: center;

    &:not(:first-child) {
      transform: translate3d(0, 100%, 0);
      -webkit-transform: translate3d(0, 100%, 0);
    }

    &.no-animation {
      transition: none;
      -webkit-transition: none;
    }
  }
  // .greeting-card-item1 {
  //   background-color: rgb(196, 108, 108) !important;
  // }
  // .greeting-card-item2 {
  //   background-color: rgb(234, 243, 155);
  // }
  // .greeting-card-item3 {
  //   background-color: rgb(144, 218, 144);
  // }
  // .greeting-card-item4 {
  //   background-color: rgb(168, 195, 226);
  // }
  // .greeting-card-item5 {
  //   background-color: rgb(245, 185, 242);
  // }

  .hide {
    display: none;
  }

  @keyframes arrowAnime {
    0% {
      opacity: 0;
      transform: translateY(20px) rotate(45deg);
    }
    100% {
      opacity: 1;
      transform: translateY(0px) rotate(45deg);
    }
  }

  ::v-deep .item-down-arrow {
    display: block;
    width: 50rpx;
    height: 50rpx;
    position: absolute;
    bottom: 36rpx;
    left: 50%;
    margin-left: -20rpx;
    border-top: 4rpx solid #795548;
    border-left: 4rpx solid #795548;
    transform: rotate(45deg);
    z-index: 9999;
    -webkit-tap-highlight-color: rgba(255, 255, 255, 0);
    animation: arrowAnime 1.5s 0.2s ease infinite;
  }
}
</style>
