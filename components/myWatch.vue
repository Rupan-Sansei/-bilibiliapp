<template>
	<view>
		<view class="box">
			<view class="title">
				<text class="left">我的追番</text>
				<text class="right">查看全部 ></text>
			</view>
			<scroll-view scroll-x="true" class="content" scroll-left="0">
				<view class="cbox">
					<image src="../static/3.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">全17话</text>
					<text class="p-type">限时免费</text>
					<view class="c-title">凡人修仙传</view>
					<view class="c-watch">看到特别篇pv</view>
				</view>
				<view class="cbox">
					<image src="../static/3.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">全17话</text>
					<text class="p-type">限时免费</text>
					<view class="c-title">凡人修仙传</view>
					<view class="c-watch">看到特别篇pv</view>
				</view>
				<view class="cbox">
					<image src="../static/3.png" mode="aspectFill" class="picture"></image>
					<text class="p-state">全17话</text>
					<text class="p-type">限时免费</text>
					<view class="c-title">凡人修仙传</view>
					<view class="c-watch">看到特别篇pv</view>
				</view>
				
			</scroll-view>
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
.box{
	.title{
		width: 100%;
		height: 90rpx;
		background-color: #1a1a1a;
		display: flex;
		align-items: center;
		justify-content:space-between;
		padding: 0 25rpx;
		.left{
			color: #ececec;
		}
		.right{
			color: #787878;
		}
	}
}
.content{
	height: 300rpx;
	background-color: #1a1a1a;
	white-space: nowrap;
	padding: 25rpx;
	border-bottom: 1rpx solid #2c2c2c;
	.cbox{
		display: inline-block;
		background-color: #1a1a1a;
		margin-right:25rpx;
		position: relative;
		.picture{
			display: block;
			width:320rpx;
			height: 200rpx;
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
			color: #e295ae;
			font-size:30rpx;
		}
		
	}
}
</style>
