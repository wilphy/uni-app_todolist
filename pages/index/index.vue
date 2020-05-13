<template>
	<view class="content">
		<!-- 状态栏 -->
		<view class="todo-header">
			<!-- 状态栏的左侧 -->
			<view class="todo-header__left">
				<text class="active-text">全部</text>
				<text>999条</text>
			</view>
			<!-- 状态栏的右侧 -->
			<view class="todo-header__right">
				<view class="todo-header__right-item active-tab">全部</view>
				<view class="todo-header__right-item">待办</view>
				<view class="todo-header__right-item">已完成</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {}
};
</script>

<style>
.todo-header {
	position: fixed;
	top: 0;
	left: 0;
	display: flex;
	align-items: center;
	padding: 0 15px;
	font-size: 12px;
	color: #333333;
	width: 100%;
	height: 45px;
	box-sizing: border-box;
	box-shadow: -1px 1px 5px 0 rgba(0, 0, 0, 0.1);
	background: #ffffff;
	z-index: 10;
}

.todo-header__left {
	width: 100%;
}

.active-text {
	font-size: 14px;
	color: #279abf;
	padding-right: 10px;
}

.todo-header__right {
	flex-shrink: 0;
	display: flex;
}

.todo-header__right-item {
	padding: 0 5px;
}

.active-tab {
	color: #279abf;
}
</style>
