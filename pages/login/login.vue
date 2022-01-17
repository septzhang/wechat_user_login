<template>
	<view class="content">
		<image class="logo" src="/static/cat.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<form action="">
			<input type="text" style="text-align: center;" placeholder-style="text-align: center" v-model = "userid" placeholder="请输入用户账号"  ><br>
			<input type="text" style="text-align: center;" placeholder-style="text-align: center" password="true" v-model = "password" placeholder="请输入密码"><br>
			<button @click="login()">登录</button>
		</form>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				userid: null,
				password: null
			}
		},
		onLoad() {

		},
		methods: {
			login(){
				console.log(this.userid + this.password)
				if(null == this.userid || null == this.password){
					this.title = '登陆失败';
				}
				if(this.userid == 'admin' && this.password == '123456'){
					this.title = '登陆成功';
					uni.redirectTo({
						url: '../home/home'
					})
					
				}else{
					this.title = '登陆失败';
				}
			}

		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	.userid{
		height: 30px;
		border: 1px #3F536E solid;
		bottom: 20px;
		top: 5px;
	}
	
	.password{
		height: 30px;
		border: 1px #3F536E solid;
		top: 20px;
	}
</style>
