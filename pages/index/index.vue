<template>
	<view class="content">
		<p>我是主页</p>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello，客官请登录'
			}
		},
		onLoad() {

		},
		methods: {
			

		}
	}
</script>

<style>
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
</style>
