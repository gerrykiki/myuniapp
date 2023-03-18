<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
			<button v-on:click="handleClick">{{buttonClick}}</button>
		</view>
	</view>
</template>

<script>
	function data() {
		return {
			title: 'Hello my name is Gerry',
			buttonClick: "Click"
		}
	}
	export default {
		data,
		onLoad() {

		},
		methods: {
			handleClick: function() {
				console.log("hi")
				uni.navigateTo({
					url:"../musicList/musicList"
				})
			}
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
		margin: 200rpx auto 50rpx auto;
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
