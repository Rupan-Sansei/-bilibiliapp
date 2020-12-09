<template>
	<view>
		<view class="box">
			<view class="left">
				<image src="../static/1.png" mode="aspectFill"></image>
				<text>13:44</text>
			</view>
			<view class="right">
				<text class="title">你好了吗</text>
				<text class="good">5万点赞</text>
				<view class="explain">
					<text class="iconfont icon-bilibili"> 葛平</text><br/>
					<text class="iconfont icon-bilibili"> 33.3万观看 2小时前</text>
				</view>
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
		display: flex;
		width: 100%;
		height: 260rpx;
		background-color: #1a1a1a;
		margin-left: 10rpx;
		border-bottom: 2rpx solid #858585;
		.left {
			position: relative;
			flex: 1;
			padding: 20rpx 20rpx 20rpx 0;

			image {
				height: 100%;
				width: 100%;
				border-radius: 10rpx;
			}

			text {
				position: absolute;
				right: 30rpx;
				bottom: 30rpx;
				color: white;
				font-size: small;
				background-color: rgba(0, 0, 0, 0.2);
			}
		}

		.right {
			padding: 20rpx 20rpx 20rpx 0;
			flex: 1;
			display: flex;
			flex-direction: column;
			overflow: hidden;

			.title {
				
				color: #eeeeee;
				width: 100%;
				height: 100rpx;
				word-break: break-all;
				text-overflow: ellipsis;
				display: -webkit-box;/**对象作为伸缩盒子模型显示 **/
				-webkit-box-orient: vertical;/** 设置或检索伸缩盒对象的子元素的排列方式 **/
				-webkit-line-clamp: 2;/** 显示的行数 **/
				overflow: hidden;
				/** 隐藏超出的内容 **/
			}
			.good {
				flex: 0;
				color: #974f39;
				font-size: x-small;
				margin: 10rpx 0;
			}
			.explain{
				color: #858585;
				text{
					display: block;
					font-size: small;
				}
			}
		}
	}
</style>
