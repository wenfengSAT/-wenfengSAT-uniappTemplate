<template>
	<view class="n-position-relative" style="width: 678rpx;margin-left: 36rpx;">
		<image :src="item.cover" mode="aspectFill" style="width: 678rpx;height: 420rpx;border-radius: 16rpx;"></image>
		<view class="n-position-absolute" style="left: 20rpx;bottom: 16rpx;">
			<text class="n-color-inverse n-size-ll n-weight-7">{{item.title}}</text>
			<text class="n-color-inverse n-size-s n-weight-7 n-lines-3" style="width: 638rpx;margin-top: 12rpx;">{{item.desc}}</text>
		</view>
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
			}
		}
	}
</script>

<style>
</style>
