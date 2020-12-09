<template>
	<view>
		<view class="box">
			<view class="title">
				<text class="left">番剧推荐</text>
				<text class="right">查看全部 ></text>
			</view>
			<view class="content">
				<view class="cbox">
					<image src="../static/2.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">205万追番</text>
					<text class="p-type">会员专享</text>
					<view class="c-title">overlord</view>
					<view class="c-watch">全15集</view>
				</view>
				<view class="cbox">
					<image src="../static/2.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">205万追番</text>
					<text class="p-type">会员专享</text>
					<view class="c-title">overlord</view>
					<view class="c-watch">全15集</view>
				</view>
				<view class="cbox">
					<image src="../static/2.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">205万追番</text>
					<text class="p-type">会员专享</text>
					<view class="c-title">overlord</view>
					<view class="c-watch">全15集</view>
				</view>
				<view class="cbox">
					<image src="../static/2.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">205万追番</text>
					<text class="p-type">会员专享</text>
					<view class="c-title">overlord</view>
					<view class="c-watch">全15集</view>
				</view>
			</view>
			<view class="refresh">
				<view class="iconfont icon-fengche size">换一换</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="less" scoped>
	.box {
		.title {
			width: 100%;
			height: 90rpx;
			background-color: #1a1a1a;
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding: 0 25rpx;

			.left {
				color: #ececec;
			}

			.right {
				color: #787878;
			}
		}
	}
	.content{
		width: 100%;
		background-color: #1a1a1a;
		display: flex;
		flex-wrap: wrap;
		padding: 10rpx;
		.cbox{
			display: inline-block;
			background-color: #1a1a1a;
			width:50%;
			height: 300rpx;
			padding: 10rpx 10rpx;
			position: relative;
			.picture{
				display: block;
				width:100%;
				height:200rpx;
				border-radius: 10rpx;
				color: #f9faf4;
			}
			.p-state{
				position: absolute;
				left: 10rpx;
				bottom: 100rpx;
				color: #f9faf4;
				font-size: 29rpx;
			}
			.p-type{
				position: absolute;
				right: 10rpx;
				top: 10rpx;
				color: #f9faf4;
				background-color: #bc647a;
				border-radius: 8rpx;
				font-size: 29rpx;
			}
			.c-title{
				color: #f9faf4;
			}
			.c-watch{
				color: #7c7c7c;
				font-size:30rpx;
			}
			
		}
	}
	.refresh{
		display: flex;
		justify-content: center;
		align-items: center;
		color:#e295ae ;
		background-color: #1a1a1a;
		border-bottom: 1rpx solid #2c2c2c;
		width: 100%;
		height: 88rpx;
		.size{
			font-size: 29rpx;
		}
	}
</style>
