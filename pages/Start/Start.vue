<template>
	<view class="list_box">
		<uni-section :title="item.title" type="line" v-for="item in list" :key="item.id">
			<uni-list>
				<uni-list-chat 
					:avatar-circle="true" 
					:ellipsis="1" 
					:clickable="true"  
					badge-positon="left" 
					badge-text="dot"
					v-for="child in item.childer" 
					:key="child.id" 
					:title="child.title"
					avatar="https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png"
					:note="child.messages" :time="child.date">
				</uni-list-chat>
				</uni-list>
		</uni-section>
		</view>
</template>

<script>
	export default {
		components: {},
		data() {
			return {
				list: [
					{
						id: 0,
						title: "Vue",
						childer: [{
								id: 1,
								title: "vue2",
								messages: "1212121",
								url: "url",
								date: "2022-01-01 12:01:01",
							},
							{
								id: 2,
								title: "vue3",
								messages: "154454545",
								url: "url",
								date: "2022-01-01 12:01:01",
							}

						]
					},
					{
						id: 3,
						title: "React",
						childer: [
							{
								id: 4,
								title: "react",
								messages: "1212121",
								url: "url",
								date: "2022-01-01 12:01:01",
							},
							{
								id: 5,
								title: "react-router-dom",
								messages: "1212121",
								url: "url",
								date: "2022-01-01 12:01:01",
							}
						]
					}
				]
			}
		}
	}
</script>

<style lang="scss">
	.list_box {
		background-color: #ccc;
	}

	.uni-section {
		margin-bottom: 30rpx;
	}

	.uni-section .uni-section-header {
		border-bottom: 1px solid #ccc;
	}

	// .uni-section-header__decoration {
	// 	background-color: red !important;
	// }
</style>
