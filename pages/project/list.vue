<!-- 项目展示 -->
<template>
	<view class="container">
		<cu-custom bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">开源项目</block>
		</cu-custom>
		
		<u-notice-bar mode="horizontal" type="primary" :list="list"></u-notice-bar>
		
		<view class="cu-bar bg-white margin-top-xs">
			<view class="action sub-title">
				<text class="text-xl text-bold text-blue text-shadow">开源项目</text>
				<text class="text-ABC text-blue">curriculum</text>
			</view>
		</view>
		
		<view class="cu-card case no-card">
		
			<view @click="goProject(item.id)" class="cu-item shadow" v-for="(item, index) in projectList" :key="index">
				<view class="image">
					<image :src="item.tImg" mode="widthFix"></image>
					<view class="cu-tag bg-gradual-orange">{{item.tabs}}</view>
					<view class="cu-bar bg-shadeBottom"> <text class="text-cut">{{item.type}}</text></view>
				</view>
				<view class="cu-list menu-avatar">
					<view class="cu-item">
						<view class="margin-lr flex-sub">
							<view class="item-name text-grey text-lg">{{item.title}}</view>
							<view class="text-gray text-sm flex justify-between">
								{{item.time}}
								<view class="text-gray text-sm">
									<text class="cuIcon-attentionfill margin-lr-xs"></text> {{item.user[0].read}}
									<text class="cuIcon-appreciatefill margin-lr-xs"></text> {{item.user[0].like}}
									<text class="cuIcon-shopfill margin-lr-xs"></text> {{item.user[0].use}}
								</view>
							</view>
						</view>
					</view>
				</view>
			</view>
		
		</view>
		
	</view>
</template>

<script>
	import request from '@/util/request.js';
	export default {
		data() {
			return {
				list:[
					'开源项目均可商用，如有需要请移步至Git或联系作者，微信：280224091'
				],
				projectList: [{
						id: 0,
						title: "数据可视化大屏电子沙盘集合",
						tImg: "https://cdn.zhoukaiwen.com/dataVIS3.png",
						type: "PC端",
						time: "2020-12-01",
						tabs: "Gitee开源",
						author: "Kevin",
						user: [{
							like: '10',
							read: '201',
							use: '15'
						}],
						introduceText: {
							projName: "数据可视化大屏电子沙盘集合",
							projSkill: "HTML/CSS/JavaScript",
							projDescribe: "数据可视化大屏电子沙盘集合，基于：html/dataV/Echarts等等，包含行业：区块链金融行业、智慧社区、智慧物业、智慧政务、智慧交通、通用模板等，包含功能：自定义字体、Css动画、WebSocket实时数据、K线折线等各种图表，iframe嵌套H5/App，替换js数据即可，满足您会议展览、业务监控、风险预警、数据分析展示等多种展示需求🔝 Gitee点个 Star 关注更新，笔芯♥️～",
							commercial: "可商用",
							projPrice: "0元",
							projUrl: "https://gitee.com/kevin_chou/dataVIS"
						},
						introduceImg: [
							"https://cdn.zhoukaiwen.com/dataVIS3.png",
							"https://cdn.zhoukaiwen.com/dataVIS1.jpeg",
							"https://cdn.zhoukaiwen.com/dataVIS2.jpeg",
							"https://cdn.zhoukaiwen.com/dataVIS6.png",
							"https://cdn.zhoukaiwen.com/dataVIS7.png",
							"https://cdn.zhoukaiwen.com/dataVIS4.jpeg"
						]
					},
					{
						id: 1,
						title: "电子商城，纯前端项目",
						tImg: "https://cdn.zhoukaiwen.com/project1.jpeg",
						type: "微信公众号/小程序",
						time: "2020-12-02",
						tabs: "可商用",
						author: "Kevin",
						user: [{
							like: '10',
							read: '201',
							use: '15'
						}],
						introduceText: {
							projName: "公众号电子商城",
							projSkill: "HTML/CSS/JavaScript",
							projDescribe: "电商平台H5页面，纯前端项目，可配置在微信公众号，H5链接中",
							commercial: "仅供学习使用",
							projPrice: "0元",
							projUrl: "咨询作者"
						},
						introduceImg: [
							"https://cdn.zhoukaiwen.com/project1.jpeg"
						]
					},
					{
						id: 2,
						title: "个人博客系统",
						tImg: "https://cdn.zhoukaiwen.com/blog2.jpg",
						type: "PC端/H5",
						time: "2021-06-15",
						tabs: "制作中",
						author: "Kevin",
						user: [{
							like: '10',
							read: '201',
							use: '15'
						}],
						introduceText: {
							projName: "个人博客系统",
							projSkill: "Vue/Ant Design",
							projDescribe: "个人博客系统，功能完善中...",
							commercial: "仅供学习使用",
							projPrice: "0元",
							projUrl: "还在完善中..."
						},
						introduceImg: [
							"https://cdn.zhoukaiwen.com/blog1.jpg",
							"https://cdn.zhoukaiwen.com/blog2.jpg",
							"https://cdn.zhoukaiwen.com/blog3.jpg"
						]
					},
					{
						id: 3,
						title: "一标三实信息管理平台",
						tImg: "https://cdn.zhoukaiwen.com/ybss_img1.png",
						type: "PC端+App",
						time: "2021-06-11",
						tabs: "不可商用",
						author: "Kevin",
						user: [{
							like: '10',
							read: '201',
							use: '15'
						}],
						introduceText: {
							projName: "一标三实信息管理平台",
							projSkill: "HTML/CSS/JavaScript/jQuery",
							projDescribe: "ToG项目，告别纸质录入、拒绝信息繁杂、实现数据共享，为解决GongAn部门制作的一款软件，同时包含App网格员端",
							commercial: "不可商用，仅可学习",
							projPrice: "0元",
							projUrl: "链接地址：咨询作者"
						},
						introduceImg: [
							"https://cdn.zhoukaiwen.com/ybss_img1.png",
							"https://cdn.zhoukaiwen.com/ybss_img2.png",
							"https://cdn.zhoukaiwen.com/ybss_img3.png",
							"https://cdn.zhoukaiwen.com/ybss_img4.png",
							"https://cdn.zhoukaiwen.com/ybss_img5.png",
							"https://cdn.zhoukaiwen.com/ybss_img6.png",
							"https://cdn.zhoukaiwen.com/ybss_img7.jpg",
							"https://cdn.zhoukaiwen.com/ybss_img8.jpg"
						]
					}
				]
			}
		},
		watch: {

		},
		mounted() {
			//this.getData();
		},
		methods: {
			getData() {
				console.log('数据加载')
				let opts = {
					url: 'json/project.json',
					method: 'get'
				};
				uni.showLoading({
					title: '加载中'
				})
				request.httpRequest(opts).then(res => {
					console.log(res);
					uni.hideLoading();
					if(res.statusCode == 200){
						this.projectList = res.data.data;
					}else{
						
					}
				});
			},
			goProject(id){
				uni.navigateTo({
					url: 'detail?proId='+id
				})
			}
		}
	}
</script>

<style scoped>
	.item-name {
		margin-bottom: 15rpx;
		display: -webkit-box;
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 1;
		overflow: hidden;
	}
</style>
