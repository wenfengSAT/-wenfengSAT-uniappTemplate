<template>
  <div
    class="greeting-card-music-player music-icon"
    v-if="musicSrc"
    :class="{ playing: isMusicPlaying }"
    @click="onMusicBtnClk"
  ></div>
</template>

<script>
export default {
  name: "greeting-card-music-player",
  components: {},
  props: {
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
      audioContext: false,
      isMusicPlaying: false,
    };
  },
  created() {},
  mounted() {
    //自动播放
    if (this.musicAutoplay) {
      this.onMusicBtnClk();
    }
  },
  methods: {
    /**
     * 控制音乐
     */
    onMusicBtnClk() {
      if (this.audioContext) {
        // 已存在

        // audioContext的状态可以判断是否正在播放
        this.isMusicPlaying = !this.audioContext.paused;
        // 切换播放或暂停
        if (this.isMusicPlaying) {
          this.audioContext.pause();
        } else {
          this.audioContext.play();
        }
      } else {
        //初始化
        this.audioContext = uni.createInnerAudioContext();

        if (this.musicAutoplay) {
          this.audioContext.autoplay = true;
        } else {
          this.audioContext.autoplay = false;
        }
        this.audioContext.loop = false;
        this.audioContext.src = this.musicSrc; //音频地址

        // this.audioContext.play();

        // 事件
        this.audioContext.onPlay(() => {
          console.log("music play");
          this.isMusicPlaying = true;
        });
        this.audioContext.onPause(() => {
          console.log("music pause");
          this.isMusicPlaying = false;
        });
        this.audioContext.onStop(() => {
          console.log("music stop");
          this.isMusicPlaying = false;
          // this.audioContext.destroy();
        });
        this.audioContext.onEnded(() => {
          console.log("music ended");
          this.isMusicPlaying = false;
          // this.audioContext.destroy();
        });

        this.audioContext.onError((res) => {
          this.isMusicPlaying = false;
          console.log(
            "music error. errMsg: ",
            res.errMsg,
            " ;errCode: ",
            res.errCode
          );
        });
      }
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

.greeting-card-music-player {
  &.music-icon {
    display: inline-block;
    position: absolute;
    right: 20rpx;
    top: 20rpx;
    width: 70rpx;
    height: 70rpx;
    background-size: 70rpx;
    z-index: 99;

    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADcAAAA3CAMAAACfBSJ0AAAAh1BMVEUAAAD///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////9qkf8RAAAALHRSTlMA6j0E4S2vQO/nFWs2Dgga+VMo7M25h3ZG02Vbmnww87NNP96oI8CMb5Lg1UAzAj8AAAKLSURBVEjHndbbkqMgEADQRpSAGsX7XeMmMcmO//99WzqzEgWMNf2QB6tOEZqGblCFHaSkQHzkqLikgQ2Hws9iemmC1saA7TZoLjTO/I/KJVF9wqtP+FRHxN1VYXItPcV3r7wmoVZ5KXMwqAM7LPU0ixVkLwU2KZRL5siB/XBQLn+smAGfwkCVxEwLPjvKNjA3wwMMnaz1X70j9xCbfu5vBxCXBxmAE4vjSMke8PI0Nmc2B0mXg2Pac8NGM3Dz5owLA5v9T0XiqI2bJR26lSHAeVwYgJP8lLKJZWQ9L5SSp/WT7lEwwOZ3Eom0XHBDXZK5eElJNK7qZk6HT6V6/fsyJiNYs3Iene5jVsM2TOs9MzXnbOWgzgAgPqmcyAzlj/C8dqcYwI+wwonMVFMmNw4jGwICsgvKn8zMxy05IAGkjcLxoTGwKC7JNQ8gvcK1q5qUXX+BwlI4SzClswpAtsYJJjufAccaJ5jszh2MoHGCyQ5GzXqCadbT7U8w3OZ5L+1Pk0/Byoher1cpn+rzqxZWoVx5fsp6YfS0XKleXS+q+jTGcnkgKYCyPrf3oa9vA+fLnkP0nYdOug8QGyDixh51V9PFYerOyRnWfyie7vtLfHCKs4H+vN/37OsO4Eb5yr0ymC6ueF+KfmLvDr+6Ie7KFfMif/Oe8X5iws2pKatNaThk+35GdGIeV9SQ/H6K99rgybynYb/tJpv+YKDArFsrpa3WiP4g+tGUEv9GebLLgKSr/jezDyH6n+i3B5mL7qv+zughZqF8O4ZYB1hoVr+ZX1xW/WpeinLNfObvKF8znwF4j+ipnQef0cMDXbQ782f7Yd6linmXEvfwfO2fAfTztX6eZ3Sk7Es3z/8D0fgrl5NXHdYAAAAASUVORK5CYII=");

    &.playing {
      background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADcAAAA3CAMAAACfBSJ0AAAAilBMVEUAAAD////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////2N2iNAAAALXRSTlMA6y3h5gVsDgg2snYaPe/UFqtTKPK4r4Z9ZUxFMAP3WpokE97NiyzOv2mjksf96K+aAAACWUlEQVRIx52W6a6CMBCFp9pi2cq+L4LiLu//ejdgIkJL4XJ+GGnypfQM0zkg0smNHAu1bYss7eKeYJUMvfG12M1tAsTO3VjzG91YpNQQVSYZLRGzQqEqpbzgnFDgRZNz4M1SNMIPAmKRB47ozGZWaMO87NASbpkhBeRSUMYvHrEJSzLxkceusKzrFMywB2u0G79qjVRYJxPVPwVoElgrpRnKETkgEc2iNx4ew+hbODxbN2LG9xI/lfanjl8rAnHhClUPfOQ8aoDDDwdKAL3UPREYp2iMacqu+z/hyP5jYsht5zrID3S1AAABB0rY9xujU27/GrcSTUccZV0/6hVw3G7qzIiDSgeAxhRzgzNJfRhzZgNgo0LM9c6EH2cmXIFO4GrAc+5jcEbAgeZCFAu48h4Pzgi4+AJOKuDy7lfCpRpYOwG3W+CuFiB7A2dgKMkG7uBDCxs4aLfut3w+kmdZyp1v0c8EsfP5zPvppFLuiDJx/aJYyu3Tme/FDWVczYqZ79MY90NaOY5TfjkPfXzwuX6A22//PfFF13X25QhTe3Pu4/67df3+GhYU6zQ5n24ZAOpkEL307h3QcL9Y6dSX4lXe334ywigy+vvs8V0pT3zd6+RoT656bXp/4h6gpfj+Hu7P6X1dPfszveWTJeDmg72v8mvk5zLMxh4/j4wnKwMxxs8joLd/zL8b3TJvVVRvnO9b8oSHj1vyi8pjAOmKvJTO5DNDQhmONeMBvSBlNg8q6EJhTrkkf+byo2tMkHeZpq7J16zL18YBij5fs5skX/N5Hvutj2fz/B/LOymzX/xZaQAAAABJRU5ErkJggg==");

      animation: rotate 3.82s linear infinite;
    }
  }
}
</style>
