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
				<button class="cx-btn">新增应用</button>
				
				<view class="cu-bar search bg-white">
					<view class="search-form round">
						<text class="cuIcon-search"></text>
						<input @focus="InputFocus" @blur="InputBlur" :adjust-position="false" type="text" placeholder="请输入应用名称" confirm-type="search"></input>
					</view>
					<view class="action">
						<button class="cu-btn bg-blue shadow-blur round">搜索</button>
					</view>
				</view>
				
				<view class="cx-app-board">
					
				</view>
				
			</view>
		</view>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
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
			
		}
	}
</script>

<style>
	@import url(./app_list.css);
</style>