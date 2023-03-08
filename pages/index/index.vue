<!-- ©️ 昶孝 版本更新网站 Author: SCC -->
<template>
	<view>
		<view class="cx-top">
			<image class="cx-logo" src="../../static/logo.png"></image>
			<view class="cx-title">AppUpdateStore</view>
		</view>
		
		<view class="cx-border">
			<view class="cx-login-border">
				<view class="cx-login-title">AppUpdateStore 版本管家</view>
				<view class="cx-login-banquan">Copyright © 2018-2023 Tianjin LoadingCreate Technology Co., Ltd</view>
				<view style="display: flex; justify-content: center;">
					<view class="cx-input">
						<input class="cx-input-id" @input="onKeyInput" placeholder="账号" />
						<input class="cx-input-id" @input="onKeyInput" password="true" placeholder="密码" />
						<button class="cx-login-btn" @click="to_app_list">登陆</button>
						<view class="cx-question">遇到问题?没有账号?</view>
					</view>
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
			to_app_list: function(){
				uni.redirectTo({
					url:"/pages/app_list/app_list"
				})
			}
		}
	}
</script>

<style>
	@import url(./index.css);
</style>
