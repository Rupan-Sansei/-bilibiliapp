<template>
	<view>
		<view class="web-box">
			<image src="../static/logo.png" mode="aspectFill"></image>
			<text v-if="type === 'web'" class="web-name">{{name}}</text>
			<text v-if="type === 'web'" class="web-people">{{watch}}</text>
			<text v-if="type === 'video'" class="web-name">{{play}}</text>
			<text v-if="type === 'video'" class="web-name2">{{comment}}</text>
			<text v-if="type === 'video'" class="web-people">{{duration}}</text>
			<text v-if="type === 'fanju'" class="web-name">{{Collection}} 追剧</text>
			<view class="web-title">
				<text class="write-title">{{title}}</text>
				<view class="web-bottom">
					<text>{{partition}}</text>
					<text>x</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			type:{
				default:"a"
			},
			name:{
				default:'up名字'
			},
			watch:{
				default:0
			},
			title:{
				default:'标题'
			},
			partition:{
				default:'分区'
			},
			play:{
				default:0
			},
			comment:{
				default:0
			},
			duration:{
				default:"3:10"
			},
			Collection:{
				default:0
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="less" scoped>
	
.web-box{
	border-radius: 10rpx;
	position: relative;
	overflow: hidden;
	margin: 9rpx;
	width: 350rpx;
	height: 300rpx;
	background-color:#141414;
	image{
		width: 100%;
		height: 200rpx
	}
	.web-name{
		position:absolute;
		left: 20rpx;
		bottom: 105rpx;
		font-size: x-small;
		color: #fcfcfc
	}
	.web-name2{
		position:absolute;
		left: 80rpx;
		bottom: 105rpx;
		font-size: x-small;
		color: #fcfcfc
		
	}
	.web-people{
		position:absolute;
		right: 20rpx;
		bottom: 105rpx;
		font-size: x-small;
		color: #fcfcfc
	}
	.web-title{
		height: 95rpx;
		width: 100%;
		display: flex;
		flex-direction: column;
		padding: 0 10rpx 10rpx 10rpx;
		.write-title{
			font-size: 40rpx;
			color: #e5e5e5;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis
		}
		.web-bottom{
			display: flex;
			justify-content: space-between;
			font-size: 30rpx;
			color: #717171;
		}
		}
}
</style>
