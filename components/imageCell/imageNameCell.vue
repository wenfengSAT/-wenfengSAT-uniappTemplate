<template>
	<view class="n-position-relative" :style="'width: 300rpx;height: 280rpx;'+boxStyle">
		<image :src="item.cover" style="width: 300rpx;height: 280rpx;border-radius: 16rpx;"></image>
		<text class="n-position-absolute n-color-inverse n-size-base n-weight-7" style="left: 20rpx;bottom: 16rpx;">{{item.title}}</text>
	</view>
</template>

<script>
	export default {
		props: {
			item: {
				type: Object,
				default: ()=>{
					return {}
				}
			},
			boxStyle: {
				type: String,
				default: ''
			}
		}
	}
</script>

<style>
</style>
