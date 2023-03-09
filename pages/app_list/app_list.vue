<template>
	<view>
		<view class="cx-top">
			<view style="display: flex; align-items: center;">
				<image class="cx-logo" src="../../static/logo.png"></image>
				<view class="cx-title">AppUpdateStore</view>
			</view>
			<view class="cx-logout" @click="backToindex">退出登录</view>
		</view>
		
		<view style="display: flex; justify-content: center;">
			<view class="cx-border">
				<view style="display: flex;justify-content: space-between;align-items: center;">
					<button class="cx-btn">新增应用</button>
					<view class="cu-bar search bg-white" style="margin-top: 20rpx;">
						<view class="search-form round">
							<text class="cuIcon-search"></text>
							<input @focus="InputFocus" @blur="InputBlur" :adjust-position="false" type="text" placeholder="请输入应用名称" confirm-type="search"></input>
						</view>
						<view class="action">
							<button class="cu-btn bg-blue shadow-blur round">搜索</button>
						</view>
					</view>
				</view>
				
				<view class="cx-line"></view>
				
				<view v-for="(item, index) in 6">
					<view class="cx-app-board">
						<view style="display: flex;flex-direction: row;justify-content: space-between;">
							<view style="display: flex; align-items: center; margin: 20rpx;">
								<image src="../../static/logo.png" class="cx-app-logo"></image>
								<view class="cx-app-title">版本管家APP</view>
								<view class="cx-top-version">1.0.1</view>
							</view>
							<view style="display: flex; align-items: center; margin: 20rpx;">
								<uni-tooltip>
									<view slot="content" style="width: 100rpx; display: flex; justify-content: center;">
										版本列表
									</view>
									<image src="../../static/list.png" class="cx-icon"></image>
								</uni-tooltip>
								<view style="margin-right: 40rpx;"></view>
								<uni-tooltip>
									<view slot="content" style="width: 100rpx; display: flex; justify-content: center;">
										编辑应用
									</view>
									<image src="../../static/set.png" class="cx-icon" @click="tapPopup"></image>
								</uni-tooltip>
								<view style="margin-right: 40rpx;"></view>
							</view>
						</view>
						<view class="cx-line" style="margin-left: 0rpx; margin-top: 10rpx;"></view>
						<view class="cx-app-font">应用ID: 384432743551045</view>
						<view class="cx-app-font">暂无描述</view>
						<view class="cx-app-font">2023-03-06T03:31:11.013504</view>
					</view>
					<view class="cx-line"></view>
				</view>	
			</view>	
		</view>
		
		<view class="cx-popup" v-show="show">
			<view class="ydt-popup-info">
				<view style="display: flex; justify-content: center; align-items: center;">
					<view>
						<view style="font-size: 40rpx; font-weight: 400; margin-top: 20rpx;">编辑应用</view>
					</view>
				</view>
				<view class="tip-line"></view>
				<view class="tip-info-board">
					<view style="font-size: 35rpx; font-weight: 500; margin-top: 20rpx;">基本信息</view>
					<view class="tip-line" style="width: 1300rpx;"></view>
				</view>
				
			</view>
		</view>
		
	</view>
</template>

<script>
	import uniTooltip from '@/uni_modules/uni-tooltip/components/uni-tooltip/uni-tooltip.vue'
	export default {
		components:{
			uniTooltip
		},
		data() {
			return {
				show: false
			}
		},
		onLoad() {
	
		},
		methods: {
			backToindex: function(){
				uni.redirectTo({
					url: "/pages/index/index"
				})
			},
			tapPopup(){
				this.show = true;
			},
			closeTap(){
				this.show = false;
			}
		}
	}
</script>

<style>
	@import url(./app_list.css);
</style>