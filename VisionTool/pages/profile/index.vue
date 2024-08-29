<template>
	<view class="container">
		<view class="profile-header">
			<image class="avatar" :src="user.userpic" />
			<view class="user-info">
				<view><text class="username">{{ user.name }}</text></view>
				<view><text class="role">{{ user.role }}</text></view>
			</view>
		</view>

		<view class="desc">
			<text class="desc-title">简介</text>
			<view>
				<text class="desc-content">{{ user.desc }}</text>
			</view>
		</view>
		
		<view class="example-image">
			<text class="desc-title">例图</text>
			<image class="example-img" mode="aspectFit" :src="user.illustration" />
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				user: {
					uid: 123,
					name: "你吃了没",
					desc: "野生摄影,野生coser,欢迎扩列野生摄影,野生coser,欢迎扩列野生摄影,野生coser,欢迎扩列",
					role: "摄影",
					userpic: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/unicloudlogo.png',
					illustration: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
				},
				messages: [
					'欢迎加入我们的社区！',
				],
			};
		},
	};
</script>

<style>
	.container {
		padding: 20px;
		background-color: #f5f5f5;
	}

	.profile-header {
		display: flex;
		align-items: center;
		margin-bottom: 20px;
	}

	.avatar {
		width: 100px;
		height: 100px;
		border-radius: 50%;
		margin-right: 20px;
	}

	.user-info {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}

	.username {
		font-size: 24px;
		font-weight: bold;
		color: #333;
	}

	.role {
		font-size: 18px;
		color: #666;
	}

	.desc {
		background-color: #fff;
		padding: 15px;
		border-radius: 8px;
		margin-bottom: 20px;
	}

	.desc-title {
		font-size: 20px;
		font-weight: bold;
		margin-bottom: 10px;
	}

	.desc-content {
		font-size: 16px;
		color: #444;
	}

	.example-image {
		background-color: #fff;
		padding: 15px;
		border-radius: 8px;
		margin-bottom: 20px;
	}

	.example-img {
		width: 100%;
		border-radius: 8px;
	}
</style>