<template>
	<view class="content">
		<!-- 标题 开始 -->
		<view class="title">
			<view class="title-left">
				<image src="https://s3.ax1x.com/2020/11/28/DyUnsI.png" mode="aspectFill"></image>
				<view class="seach">
					<text class="iconfont icon-sousuo"></text>
				</view>
			</view>
			<view class="title-right">
				<text class="iconfont icon-youxi"></text>
				<text class="iconfont icon-xinjian"></text>
			</view>

		</view>
		<!-- 标题 结束 -->

		<!-- 分段器 开始 -->
		<view>
			<view :class=" scrollTop > 40 ? 'fixed':''">
				<uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" style-type="text" active-color="#eb7093"
				 color="#9f9f9f"></uni-segmented-control>
			</view>
			<view >
				<!-- 直播 开始 -->
				<view v-if="current === 0">
					<!-- 直播分类 开始 -->
					<view class="type">
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
						<view class="box">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							英雄联盟
						</view>
					</view>
					<!-- 直播分类 结束 -->
					
					<!-- 我的关注 开始 -->
					<view class="watch">
						<view class="watch-title">
							<view class="left-title">
								<text class="big">我的关注</text>
								<text class="color">2</text>
								人正在直播  |||
								
							</view>
							<text class="right-title">查看全部></text>
						</view>
						<view class="watch-content">
							<view class="watch-box">
								<image src="../../static/logo.png" mode="aspectFill"></image>
								<view class="write">
									<text>哔哩哔哩英雄联盟</text>
									<view class="">
										英雄联盟 66.6万
									</view>
								</view>
							</view>
							<view class="watch-box">
								<image src="../../static/logo.png" mode="aspectFill"></image>
								<view class="write">
									<text>哔哩哔哩英雄联盟</text>
									<view class="">
										英雄联盟 66.6万
									</view>
								</view>
							</view>
						</view>
					</view>
					<!-- 我的关注 结束 -->
					
					<!-- 推荐直播  开始-->
					<view class="webcast">
						<view class=" web-title">
							<text class="iconfont icon-bilibili"></text>
							推荐直播
						</view>
						<view class="web-content">
							<web-card type='web' name="港湾少女" title="你今天开心吗" partition="聊天电台" watch="12"></web-card>
							<web-card type='web'></web-card>
							<web-card type='web'></web-card>
							<web-card type='web'></web-card>
							<web-card type='web'></web-card>
							<web-card type='web'></web-card>
						</view>
					</view>
					<!-- 推荐直播  结束-->
				</view>
				<!-- 直播 结束 -->

				<!-- 推荐 开始 -->
				<view v-if="current === 1">
					<!-- 轮播图 开始 -->
					<view class="picture">
						<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
							<swiper-item>
								<view class="swiper-item"><image src="../../static/1.png" mode="widthFix"></image></view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item"><image src="../../static/2.png" mode="widthFix"></image></view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item"><image src="../../static/3.png" mode="widthFix"></image></view>
							</swiper-item>
						</swiper>
					</view>
					<!-- 轮播图 结束 -->
					
					<!-- 推荐 内容开始 -->
					<view class="recommend-content">
						<web-card type="video"></web-card>
						<web-card type="video"></web-card>
						<web-card type="video"></web-card>
						<web-card type="video"></web-card>
						<web-card type="video"></web-card>
						<web-card type="video"></web-card>
					</view>
					<!-- 推荐 内容结束 -->
				</view>
				<!-- 推荐 结束 -->

				<!-- 热门 开始 -->
				<view v-if="current === 2">
					<!-- 头部 开始 -->
					<view class="hot-title">
						<view class="hot-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>排行榜</text>
						</view>
						<view class="hot-type">
							<image src="../../static/logo.png"  mode="aspectFill"></image>
							<text>每周必看</text>
						</view>
						<view class="hot-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>入站必刷</text>
						</view>
					</view>
					<!-- 头部 结束-->
					
					<!-- 内容 开始 -->
					<view class="hot-content">
						<m-card></m-card>
						<m-card></m-card>
						<m-card></m-card>
						<m-card></m-card>
						<m-card></m-card>
					</view>
					<!-- 内容 结束 -->
				</view>
				<!-- 热门 结束 -->
				
				<!-- 追番 开始 -->
				<view v-if="current === 3">
					<!-- 轮播图开始 -->
					<view class="picture">
						<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
							<swiper-item>
								<view class="swiper-item"><image src="../../static/1.png" mode="widthFix"></image></view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item"><image src="../../static/2.png" mode="widthFix"></image></view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item"><image src="../../static/3.png" mode="widthFix"></image></view>
							</swiper-item>
						</swiper>
					</view>
					<!-- 轮播图结束 -->
					
					<!-- 分类 开始-->
					<view class="nav-title">
						<view class="nav-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>番剧</text>
						</view>
						<view class="nav-type">
							<image src="../../static/logo.png"  mode="aspectFill"></image>
							<text>国创</text>
						</view>
						<view class="nav-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>时间表</text>
						</view>
						<view class="nav-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>索引</text>
						</view>
						<view class="nav-type">
							<image src="../../static/logo.png" mode="aspectFill"></image>
							<text>十月新番</text>
						</view>
					</view>
					<!-- 分类 结束-->
					
					<!-- 我的追番 开始 -->
					<my-watch></my-watch>
					<!-- 我的追番 结束 -->
					
					<!-- 番剧推荐 开始 -->
					<recommend></recommend>
					<!-- 番剧推荐 结束 -->
				</view>
				<!-- 追番 结束 -->
				
				<view v-if="current === 4">
					影视
				</view>
			</view>
		</view>
		<!-- 分段器 开始 -->

	</view>
</template>

<script>
	import uniSegmentedControl from "@/components/uni-segmented-control/uni-segmented-control.vue"
	import webCard from '@/components/webCard.vue'
	import mCard from '@/components/mCard.vue'
	import myWatch from '@/components/myWatch.vue'
	import recommend from '@/components/recommend.vue'
	export default {
		components: {
			uniSegmentedControl,
			webCard,
			mCard,
			myWatch,
			recommend
		},
		data() {
			return {
				items: ['直播', '推荐', '热门', '追番', '影视'],
				current: 3,
				scrollTop:0
			}
		},
		onLoad() {

		},
		methods: {
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex;
				}
			}
		},
		//监听滑动高度
		onPageScroll(res){
			this.scrollTop = res.scrollTop;//距离页面顶部距离
			// console.log(this.scrollTop );
		},
	}
</script>

<style lang="less" scoped>
	// 分段器的固定定位
	.fixed{
		position: fixed;
		top: 0;
		width: 100%;
		z-index: 2;
		background-color: white;
	}
	// 标题开始
	.content{
		width: 100%;
		height: 100vh;
		// background-color: #030303;
	}
	.title {
		// margin-top: 50rpx;
		// margin-top: 180rpx;
		display: flex;
		width: 100vh;
		height: 100rpx;
		background-color: #141414;

		.title-left {
			display: flex;
			justify-content: center;
			align-items: center;
			padding: 10rpx;

			image {
				height: 80rpx;
				width: 80rpx;
				border-radius: 50%;
				background-color: black;
			}

			.seach {
				width: 400rpx;
				height: 70rpx;
				border-radius: 40rpx;
				background-color: #1e1e1e;
				color: red;
				margin-left: 40rpx;

				text {
					padding-left: 20rpx;
					height: 100%;
					width: 80rpx;
					font-size: 600;
					color: #5a5a5a;
					vertical-align: middle;
				}
			}
		}

		.title-right {
			display: flex;
			justify-content: center;
			align-items: center;

			text {
				margin: 10rpx 20rpx;
				color: #979797;
				font-size: 60rpx
			}
		}
	}
	// 标题结束

	// 分段器开始
	//直播分区 开始
	.type {
		display: flex;
		flex-wrap: wrap;
		margin: 20rpx 10rpx;
		background-color: #141414;
		border-radius: 10rpx;
		view {
			width: 20%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			font-size: 30rpx;
			color: #e8e8e8;
			margin: 10rpx 0;
			image {
				display: block;
				width: 90rpx;
				height: 90rpx;

			}
		}
	}
	// 我的关注 开始
	.watch{
		margin: 20rpx 10rpx;
		background-color: #141414;
		color: #efefef;
		.watch-title{
			display: flex;
			justify-content: space-between;
			.left-title{
				.big{
					font-weight: 600;
					margin-right: 10rpx;
				}
				.color{
					color:#ee7195 ;
				}
			}
			.right-title{
				font-size: 35rpx;
			}
		}
		.watch-content{
			display: flex;
			justify-content: space-between;
			padding: 30rpx 10rpx;
			.watch-box{
				border: 2rpx solid #2a2a2a;
				display: flex;
				align-items: center;
				width: 48%;
				height: 150rpx;
				border-radius: 10rpx;
				image{
					margin-left: 10rpx;
					height: 90rpx;
					width: 90rpx;
					border-radius: 50%;
					background-color: pink;
				}
				.write{
					margin-left: 10rpx;
					white-space:nowrap;
					overflow: hidden;
					text-overflow: ellipsis;
					view{
						font-size: 30rpx;
						margin-top: 10rpx;
					}
				}
			}
		}
	}
	// 我的关注 结束
	
	//推荐直播 开始
	.webcast{
		margin: 20rpx 10rpx;
		.web-title{
			vertical-align: middle;
			text{
				color: #ee7195;
				margin-right: 10rpx;
			}
		}
		.web-content{
			display: flex;
			flex-wrap: wrap;
			
		}
	}
	//推荐直播 结束
	//直播分区 结束
	
	// 推荐分区 开始
	.picture{
		margin: 20rpx 10rpx;
		overflow: hidden;
		border-radius: 10rpx;
		image{
			width: 100%;
			height: 100% ;
		}
	}
	.recommend-content{
		margin: 20rpx 10rpx;
		display: flex;
		flex-wrap: wrap;
	}
	// 推荐分区 结束
	
	// 热门分区 开始
	.hot-title{
		display: flex;
		width: 100%;
		height: 200rpx;
		background-color: #1a1a1a;
		.hot-type{
			width: 33.33%;
			height: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			color: #aaaaaa;
			font-size: small;
			image{
				height: 100rpx;
				width: 100rpx;
				border-radius: 50%;
				margin-bottom: 10rpx;
			}
		}
	}
	.hot-content{
		background-color: #1a1a1a;
	}
	// 热门分区 结束
	
	//追番分区 开始
	.nav-title{
		display: flex;
		width: 100%;
		height: 200rpx;
		background-color: #1a1a1a;
		border-bottom: 1rpx solid #2c2c2c;
		.nav-type{
			width: 20%;
			height: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			color: #aaaaaa;
			font-size:x-small;
			image{
				height: 80rpx;
				width: 80rpx;
				border-radius: 50%;
				margin-bottom: 10rpx;
			}
		}
	}
	//追番分区 结束
	// 分段器结束
</style>
