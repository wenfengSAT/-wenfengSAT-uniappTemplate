<template>
	<view>
		<page1 v-if="PageCur=='page1'"></page1>
		<page2 v-if="PageCur=='page2'"></page2>
		<page3 v-if="PageCur=='page3'"></page3>
		<page4 v-if="PageCur=='page4'"></page4>
		<page5 v-if="PageCur=='page5'"></page5>

		<view class="box">
			<view class="cu-bar tabbar bg-white shadow foot">
				<view class="action" @click="NavChange" data-cur="page1">
					<view class='cuIcon-cu-image'>
						<image v-if="PageCur=='page1'" src="../../static/tabBar/page1_cur.png"></image>
						<image v-if="PageCur != 'page1'" src="../../static/tabBar/page1.png"></image>
					</view>
					<view :class="PageCur=='page1'?'color_main':'text-gray'">首页</view>
				</view>

				<view class="action" @click="NavChange" data-cur="page2">
					<view class='cuIcon-cu-image'>
						<image v-if="PageCur=='page2'" src="../../static/tabBar/page2_cur.png"></image>
						<image v-if="PageCur != 'page2'" src="../../static/tabBar/page2.png"></image>
					</view>
					<view :class="PageCur=='page2'?'color_main':'text-gray'">技术栈</view>
				</view>

				<view @click="NavChange" class="action text-gray add-action" data-cur="page3">
					<image class="logo_btn" mode="widthFix" src="../../static/tabBar/page3_cur.png"></image>
					<view :class="PageCur=='page3'?'color_main':'text-gray'">组件模板</view>
				</view>

				<view class="action" @click="NavChange" data-cur="page4">
					<view class='cuIcon-cu-image'>
						<view class="cu-tag badge">{{message}}</view>
						<image v-if="PageCur=='page4'" src="../../static/tabBar/page4_cur.png"></image>
						<image v-if="PageCur != 'page4'" src="../../static/tabBar/page4.png"></image>
					</view>
					<view :class="PageCur=='page4'?'color_main':'text-gray'">文章资讯</view>
				</view>

				<view class="action" @click="NavChange" data-cur="page5">
					<view class='cuIcon-cu-image'>
						<view class="cu-tag badge">
							<!-- 红点 -->
						</view>
						<image v-if="PageCur=='page5'" src="../../static/tabBar/page5_cur.png"></image>
						<image v-if="PageCur != 'page5'" src="../../static/tabBar/page5.png"></image>
					</view>
					<view :class="PageCur=='page5'?'color_main':'text-gray'">个人中心</view>
				</view>

			</view>
		</view>

	</view>
</template>

<script>
	import page1 from "./page1.vue"; //首页
	import page2 from "./page2.vue"; //技术视频
	import page3 from "./page3.vue"; //宅家学
	import page4 from "./page4.vue"; //资讯
	import page5 from "./page5.vue"; //个人中心
	export default {
		components: {
			page1,
			page2,
			page3,
			page4,
			page5
		},
		data() {
			return {
				PageCur: 'page3',
				message: '2',
				openId: '',
				access_token: '',
				tip: "我是提示",
				duration: 1

			};
		},
		// 分享小程序
		onShareAppMessage(res) {
			return {
				title: '学技术·做软件·找案例·寻合作，快来「7he丶Thy」吧！',
			};
		},
		onLoad() {
			//获取退出时的tabbar记录
			// uni.getStorage({
			// 	key: 'PageCur',
			// 	success: function(res) {
			// 		that.PageCur = res.data;
			// 	},
			// 	fail: function(res) {}
			// });
		},
		methods: {
			NavChange: function(e) {
				console.log(e.currentTarget.dataset.cur)

				this.PageCur = e.currentTarget.dataset.cur;

				if (this.PageCur == 'page1') {
					// document.title = 'page1'
				} else if (this.PageCur == 'page2') {
					// document.title = 'page2'
				} else if (this.PageCur == 'page3') {
					// document.title = 'page3'
				} else if (this.PageCur == 'page4') {
					// document.title = 'page4'
				} else if (this.PageCur == 'page5') {
					// document.title = 'page5'
				}

				// uni.setStorage({
				// 	key: 'PageCur',
				// 	data: this.PageCur,
				// 	success: function() {
				// 		console.log('保存成功！');
				// 	}
				// });
			},
			NavChange_xd: function() {
				uni.navigateTo({
					url: 'publish',
					animationType: 'slide-in-bottom',
					animationDuration: 200
				});
			}
		}
	}
</script>

<style lang="scss">
	.box {
		margin: 20upx 0;
	}

	.box view.cu-bar {
		margin-top: 20upx;
	}

	.logo_btn {
		width: 38*2rpx;
		height: 38*2rpx;
		position: absolute;
		z-index: 2;
		border-radius: 50%;
		top: -40rpx;
		left: 0rpx;
		right: 0;
		margin: auto;
		padding: 0;
	}

	.cu-bar.tabbar .action.add-action {
		padding-top: 56rpx !important;
	}
</style>
