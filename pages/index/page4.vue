<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<navigator url="/pages/card/wedding/index" open-type="navigate">
		     <view class="title">婚礼祝福</view>
		</navigator>
		<navigator url="/pages/card/birthday/index" open-type="navigate">
		     <view class="title">生日祝福</view>
		</navigator>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
