<template lang="html">
	<Panel :title="title" :class="[$style.panel, cname]">
		<ul :class="[$style.content, 'clearfix']">
			<li :class="$style.item" v-for="item in items" :key="item.menuWord">
				<img :src="item.img" alt="404">
				<strong>{{ item.menuWord }}</strong>
				<i>{{  item.trait }}</i>
			</li>
		</ul>
	</Panel>
</template>

<script>
	import Panel from './../core/panel.vue'
	export default {
		data () {
			return {}
		},
		props: {
			title: {
				type: String,
				default: ''
			},
			items: {
				type: Array,
				default: []
			},
			cname: {
				type: String,
				default: ''
			}
		},
		methods: {

		},
		components: {
			 Panel,
		}
	}
</script>

<style lang="scss" module>
	.panel {
		h4 {
			font-weight: 700;
		}
		.content {
			li {
				float: left;
				width: 20%;
				text-align: center;
				overflow: hidden;
				text-overflow: ellipsis;
				white-space: nowrap;
				font-size: 0px;
				padding-bottom: 20px;
				img {
					width: 90px;
					height: 90px;
					display: block;
					margin: 0px auto;
				}
				strong {
					font-size: 26px;
					display: block;
					color: #666;
					padding-top: 12px;

				}
				i {
					font-size: 22px;
					color: #ff8014;
					line-height: 60px;
				}
			}
		}
	}
</style>