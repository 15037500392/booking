<template>
	<view>
		{{name}}
	</view>
</template>

<script lang="ts">
	import Vue from 'vue'
	import Component from 'vue-class-component'
	@Component({})
	export default class Home extends Vue{
		private name:string = '张三'
	}
</script>

<style lang="less" scoped>
</style>
