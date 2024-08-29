<template>
	<view>
		<swiper class="swiper-box" :indicator-dots="true" :autoplay="true" @change="swiperchange">
			<swiper-item v-for="(item ,index) in swiperinfo" :key="index">
				<view class="swiper-item">
					<image :mode="aspectFit" :src="item.url"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
	<view class="container">
		<uni-section title="日程表" type="line"></uni-section>
		<view>
			<uni-calendar class="uni-calendar--hook" :selected="info.selected" :showMonth="true" @change="calendarchange"
				@monthSwitch="monthSwitch" />
		</view>
	</view>
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				swiperinfo: [{
						url: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					},
					{
						url: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					},
					{
						url: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					},
					{
						url: 'https://qiniu-web-assets.dcloud.net.cn/unidoc/zh/shuijiao.jpg',
					}
				],
				info: {
					selected: [{
						date: '2024-08-27',
						info: '已预约',
						data: {
							custom: '自定义信息',
							name: '自定义消息头',
						}
					}]
				}
			};
		},
		onReady() {},
		methods: {
			swiperchange(e) {
				this.current = e.detail.current;
			},
			calendarchange(e) {
				
			},
			monthSwitch(e) {
				
			}
		}
	};
</script>

<style lang="scss">
	.example-body {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: row;
	}

	.calendar-button {
		flex: 1;
		font-weight: bold;
		font-size: 32rpx;
	}

	.swiper-box {
		height: 200px;
	}

	.swiper-item {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 200px;
		color: #fff;
	}
</style>