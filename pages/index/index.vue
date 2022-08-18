<template>
	<uni-section title="分类" subTitle="使用单一分栏创建基础的栅格布局" type="line">
		<view class="example-body">
			<uni-row class="demo-uni-row" >
				<uni-col :span="12" v-for="item in list" :key="item.badge">
					<uni-card padding="0" spacing="0" :is-shadow="true">
						<template v-slot:cover>
							<view class="custom-cover">
								<image class="cover-image" mode="aspectFill" :src="item.url">
								</image>
								<view class="cover-content">
									<text class="uni-subtitle uni-white">{{item.text}}</text>
								</view>
							</view>
						</template>
					</uni-card>
				</uni-col>
			</uni-row>
		</view>
	</uni-section>
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				cover: 'https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/094a9dc0-50c0-11eb-b680-7980c8a877b8.jpg',
				dynamicList: [],
				list: [{
						url: '/static/c1.png',
						text: 'Grid 1',
						badge: '0',
						type: "primary"
					},
					{
						url: '/static/c2.png',
						text: 'Grid 2',
						badge: '1',
						type: "success"
					},
					{
						url: '/static/c3.png',
						text: 'Grid 3',
						badge: '99',
						type: "warning"
					},
					{
						url: '/static/c4.png',
						text: 'Grid 3',
						badge: '4',
						type: "warning"
					},
					{
						url: '/static/c5.png',
						text: 'Grid 3',
						badge: '6',
						type: "warning"
					},
					{
						url: '/static/c6.png',
						text: 'Grid 3',
						badge: '8',
						type: "warning"
					}
				]
			}
		},

	}
</script>
<style lang="scss">
	.cover-content{
		background-color: rgba(0,0,0,.4);
		width: 100%;
		overflow: hidden;
		white-space: nowrap;
		position: absolute;
		bottom: 0;
	}
	.cover-image{
		display: block;
		width: 100%;
	}
</style>
