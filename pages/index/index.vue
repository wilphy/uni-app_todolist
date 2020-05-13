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

		<!-- 内容 -->
		<view class="todo-content">
			<view class="todo-list todo--finsh">
				<view class="todo-list__checkbox"><view class="checkbox"></view></view>
				<view class="todo-list__content">我的待办事项</view>
			</view>
		</view>
		<view class="todo-content">
			<view class="todo-list">
				<view class="todo-list__checkbox"><view class="checkbox"></view></view>
				<view class="todo-list__content">我的待办事项</view>
			</view>
		</view>

		<!-- 创建按钮 -->
		<view class="create-todo"><text class="iconfont icon-jiahao"></text></view>

		<!-- 输入框 -->
		<view class="create-content">
			<view class="create-content-box">
				<view class="create-input"><input type="text" value="" placeholder="请输入待办事项" /></view>
				<view class="create-button">创建</view>
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
@import url('../../common/icon.css');
.todo-header {
	/* position: fixed;
	top: 0;
	left: 0; */
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
	/* z-index: 10; */
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

.todo-content {
	position: relative;
}

.todo-list {
	position: relative;
	display: flex;
	align-items: center;
	padding: 15px;
	margin: 15px;
	border-radius: 10px;
	font-size: 14px;
	color: #0c3854;
	background-color: #abcfed;
	box-shadow: -1px 1px 5px 1px rgba(0, 0, 0, 0.1), -1px 2px 1px 0 rgba(255, 255, 255) inset;
	overflow: hidden;
}

.todo-list:after {
	position: absolute;
	content: '';
	top: 0;
	bottom: 0;
	left: 0;
	width: 5px;
	background-color: #f06;
}

.todo-list__checkbox {
	padding-right: 15px;
}

.checkbox {
	width: 20px;
	height: 20px;
	border-radius: 50%;
	background-color: #ffffff;
	box-shadow: 0 0 5px 1px rgba(0, 0, 0, 0.1);
}

.todo--finsh .checkbox {
	position: relative;
	background-color: #eee;
}
.todo--finsh .checkbox:after {
	content: '';
	position: absolute;
	width: 10px;
	height: 10px;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	margin: auto;
	background-color: #cfebfd;
	border-radius: 50%;
	box-shadow: 0 0 2px 0px rgba(0, 0, 0, 0.2) inset;
}

.todo--finsh .todo-list__content {
	color: #999;
}

.todo--finsh.todo-list:before {
	content: '';
	position: absolute;
	top: 0;
	bottom: 0;
	left: 40px;
	right: 10px;
	height: 2px;
	margin: auto 0;
	background-color: #aaa;
}

.todo--finsh.todo-list:after {
	background-color: #ccc;
}

.create-todo {
	display: flex;
	justify-content: center;
	align-items: center;
	position: fixed;
	bottom: 20px;
	left: 0;
	right: 0;
	width: 50px;
	height: 50px;
	margin: 0 auto;
	border-radius: 50%;
	/* font-size: 14px; */
	background-color: #96f;
	box-shadow: -1px 1px 5px 2px rgba(0, 0, 0, 0.1), -1px 1px 1px 0 rgba(255, 255, 255) inset;
}

.icon-jiahao {
	font-size: 30px;
	color: #ddd;
}

.create-content {
	position: fixed;
	bottom: 95px;
	left: 20px;
	right: 20px;
}
.create-content:after {
	content: '';
	position: absolute;
	left: 0;
	right: 0;
	bottom: -8px;
	margin: 0 auto;
	width: 20px;
	height: 20px;
	background-color: #f69;
	transform: rotate(45deg);
	box-shadow: 1px 1px 5px 2px rgba(0, 0, 0, 0.1);
	z-index: -1;
}

.create-content-box {
	display: flex;
	align-items: center;
	padding: 0 15px;
	padding-right: 0;
	border-radius: 50px;
	background-color: #f69;
	box-shadow: -1px 1px 5px 2px rgba(0, 0, 0, 0.1), -1px 1px 1px 0 rgba(255, 255, 255) inset;
	z-index: 2;
}

.create-content-box:after {
	content: '';
	position: absolute;
	right: 0;
	left: 0;
	bottom: -8px;
	margin: 0 auto;
	width: 20px;
	height: 20px;
	background-color: #f69;
	transform: rotate(45deg);
}

.create-input {
	width: 100%;
	padding-right: 15px;
	color: #add8e6;
}

.create-button {
	display: flex;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
	width: 80px;
	height: 50px;
	border-radius: 50px;
	font-size: 16px;
	color: #fff;
	box-shadow: -2px 0px 2px 1px rgba(0, 0, 0, 0.1);
}
</style>
