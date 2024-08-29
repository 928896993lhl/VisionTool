<template>
	<uni-collapse accordion >
		<uni-collapse-item v-for="(order ,orderId) in orderlist" :key="orderId" >
			<template v-slot:title>
				<view class="profile-header">
					<view class="order-info">
						<view><text class="theme">{{order.theme}}</text></view>
						<view><text class="shootingdate">{{order.shootingdate}}</text></view>
					</view>
				</view>
			</template>
			<view class="content">
				<uni-steps :options="steps" active-color="#007AFF" :active="order.active" />
			</view>
		</uni-collapse-item>
	</uni-collapse>
</template>

<script>
	export default {
		data() {
			return {
				orderlist: [{
						orderId: 123,
						theme: "边缘行者lucy",
						shootingdate: "2024.08.22",
						active: 1
					},
					{
						orderId: 222,
						theme: "薇尔莉特",
						shootingdate: "2024.09.22",
						active: 2
					},
					{
						orderId: 333,
						theme: "宵宫",
						shootingdate: "2024.12.22",
						active: 3
					},
				],
				steps: [{
					title: '已预约'
				}, {
					title: '拍摄日'
				}, {
					title: '待返图'
				}, {
					title: '已完成'
				}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.profile-header {
		display: flex;
		align-items: center;
		margin-bottom: 20px;
		margin-left: 20px;
		margin-top: 20px;
	}

	.avatar {
		width: 50px;
		height: 50px;
		border-radius: 50%;
		margin-right: 20px;
		margin-left: 20px;
	}

	.order-info {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}

	.theme {
		font-size: 20px;
		font-weight: bold;
		color: #333;
	}

	.shootingdate {
		font-size: 16px;
		color: #666;
	}

	.example-body {
		flex-direction: column;
		flex: 1;
	}

	.content {
		padding: 15px;
	}

	.text {
		font-size: 14px;
		color: #666;
		line-height: 20px;
	}

	.button {
		// margin-top: 10px;
		margin: 10px;
		margin-bottom: 0;
	}
</style>