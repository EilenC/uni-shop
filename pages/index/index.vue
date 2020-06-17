<template>
	<view class="">
		<!-- 		<view>
			<QSGradientSwiper autoplay circular ref="QSGradientSwiper"></QSGradientSwiper>
		</view> -->
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" circular :interval="interval">
			<swiper-item v-for="(url) in images" :key="url">
				<view class="swiper-item">
					<image :src="url"></image> 
				</view>
			</swiper-item>
		</swiper>
		<!-- 导航区域 -->
		<view class="nav">
			<view class="nav_item">
				<view class="iconfont icon-ziyuan"></view>
				<text>在线超市</text>
			</view>
			<view class="nav_item">
				<view class="iconfont icon-tupian"></view>
				<text>社区图片</text>
			</view>
			<view class="nav_item">
				<view class="iconfont icon-guanyuwomen"></view>
				<text>联系我们</text>
			</view>
			<view class="nav_item">
				<view class="iconfont icon-shipin"></view>
				<text>学习视频</text>
			</view>
		</view>
	</view>
</template>

<script>
	import QSGradientSwiper from '@/components/QS-Gradient-Swiper/QS-Gradient-Swiper-vue.vue';
	export default {
		data() {
			return {
				indicatorDots:true,
				autoplay:true,
				interval:2500,
				images:[
					'http://imgsrc.baidu.com/forum/w%3D580/sign=791a660d9c2397ddd679980c6983b216/591f9758d109b3de80a0bb82c1bf6c81810a4c89.jpg',
					'http://imgsrc.baidu.com/forum/w%3D580/sign=e8b1d9c798cad1c8d0bbfc2f4f3c67c4/ab5e4efbfbedab64dbb08428fa36afc37b311eed.jpg',
					'http://imgsrc.baidu.com/forum/w%3D580/sign=a06847cac5fcc3ceb4c0c93ba244d6b7/85d3bc014a90f60394f557af3412b31bb151ed67.jpg'
				]
			}
		},
		components: {
			QSGradientSwiper
		},
		onLoad() {

		},
		onReady() {
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.swiper-item {
		width: 750rpx;
		height: 380rpx;
	}

	.swiper-item image {
		height: 100%;
		width: 100%;
	}
	.nav{
		display: flex;
		.nav_item{
			width: 25%;
			text-align: center;
			view{
				width: 120rpx;
				height: 120rpx;
				background-color: #b50e03;
				border-radius: 60rpx;
				margin: 10px auto;
				line-height: 120rpx;
				color: #FFFFFF;
				font-size: 50rpx;
			}
			text{
				font-size: 30rpx;
			}
		}
	}
</style>
