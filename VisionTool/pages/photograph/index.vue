<template>
	<view class="content" v-for="(item ,index) in infolist" :key="index">
		<uni-card :title="item.name" :sub-title="item.desc" :extra="item.extra" :thumbnail="item.userpic">
			<image mode="aspectFit" :src="item.illustration"></image>
			<view slot="actions" class="card-actions">
				<view class="card-actions-item" @click="actionsClick(item)">
					<uni-icons type="heart" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">点赞</text>
				</view>
				<view class="card-actions-item" @click="onClick(item)">
					<uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
					<text class="card-actions-item-text">预约</text>
				</view>
			</view>
		</uni-card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				infolist: [{
						uid: 123,
						name: "你吃了没",
						desc: "野生摄影,野生coser,欢迎扩列野生摄影,野生coser,欢迎扩列野生摄影,野生coser,欢迎扩列",
						extra: "互勉",
						userpic: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/unicloudlogo.png',
						illustration: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					},
					{
						uid: 1234,
						name: "我吃了呀",
						desc: "野生摄影2号,野生coser,欢迎扩列",
						extra: "付费",
						userpic: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/unicloudlogo.png',
						illustration: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					},
					{
						uid: 12224,
						name: "我吃了呀",
						desc: "野生摄影3号,野生coser,欢迎扩列",
						extra: "付费",
						userpic: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/unicloudlogo.png',
						illustration: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			onClick(item) {
				console.log("todo:业务逻辑,弹窗摄影时间表");
				console.log(item)
			},
			actionsClick(item) {
				console.log("todo:业务逻辑,该摄影点赞数+1");
				console.log(item)
			}
		}
	}
</script>

<style>
	.content {
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
	}

	.card-actions {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
		height: 45px;
		border-top: 1px #eee solid;
	}

	.card-actions-item {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.card-actions-item-text {
		font-size: 12px;
		color: #666;
		margin-left: 5px;
	}
</style>