<template>
	<view class="login-container">
		<view>
			<view class="title">用户名：</view>
			<input class="c-uni-input" focus placeholder="请输入用户手机号" v-model="username" />
		</view>
		<view class="spliter"></view>
		<view>
			<view class="title">密码：</view>
			<input class="c-uni-input" password type="text" placeholder="请输入密码" v-model="password" />
		</view>
		<view class="spliter"></view>
		<view class="buttons">
			<button type="primary" v-on:click="login">登录</button>
			<button type="default" v-on:click="goHome">不登录，直接去首页</button>
		</view>
	</view>
</template>

<script>
	import LoginService from '@/api/login/index.js'
	import UserService from '@/api/user/index.js'
	import Session from '@/plugins/session'
	export default {
		data() {
			return {
				username: '15927089230',
				password: 'abc123__'
			}
		},
		methods: {
			async login() {
				let res = await LoginService.login({
					username: this.username,
					password: this.password,
				})
				console.log(res)
				if (res.statusCode === 200) {
					let token = res.data.token

					let auth = {
						token: res.data.token
					}

					Session.setToken(auth)

					let userRep = await UserService.getUserInfo()
					if (userRep.statusCode === 200) {
						let auth = {
							token: res.data.token,
							userName: userRep.data.username ? userRep.data.username : '',
							realName: userRep.data.realName ? userRep.data.realName : '',
							nickName: userRep.data.nickName ? userRep.data.nickName : '',
							userId: userRep.data.userId,
							loginName: userRep.data.loginName,
							phone: userRep.data.phone,
							avatar: userRep.data.avatar ? userRep.data.avatar : ''
						}
						Session.setToken(auth)
						uni.switchTab({
							url: "/pages/buy/retail/index"
						})
					}else {
					uni.showToast({
						icon: 'none',
						title: res.errorMessage
					})
				}
				} else {
					uni.showToast({
						icon: 'none',
						title: res.errorMessage
					})
				}
			},
			goHome(){
				uni.switchTab({
					url: "/pages/buy/retail/index"
				})
			}
		}
	}
</script>

<style scoped>
	.login-container {
		margin: 20rpx 30rpx;
		width: 750rpx; 
	}
	.c-uni-input {
		border: gray 1px solid;
		font-size: 18px;
		height: 80rpx !important;
	}
	.spliter{
		height: 20rpx;
	}
	.buttons{
		display: flex;
		
	}
</style>
