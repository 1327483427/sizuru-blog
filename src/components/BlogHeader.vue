<template>
  <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
    mode="horizontal"
    :ellipsis="false"
    @select="handleSelect"
  >
    <el-menu-item index="0">
      <span class="logo"></span>
      <div class="div-separator"></div>
    </el-menu-item>
    <el-menu-item index="1">
      <div>首页</div>
    </el-menu-item>

    <el-menu-item>
      <div>技术</div>
    </el-menu-item>

    <el-menu-item>
      <div>生活</div>
    </el-menu-item>

    <el-menu-item>
      <div>音乐</div>
    </el-menu-item>

    <el-menu-item>
      <div>休闲地</div>
    </el-menu-item>
    <div class="flex-grow" />
    <el-input
      v-model="searchText"
      class="serach-input"
      placeholder="搜索"
      :prefix-icon="Search"
    />

    <el-sub-menu index="2" popper-offset="-5">
      <template #title>
        <el-icon class="el-icon-setting">
          <Calendar />
        </el-icon>
      </template>
      <el-menu-item index="2-1">新浪微博</el-menu-item>
      <el-menu-item index="2-2">github</el-menu-item>
      <el-menu-item index="2-3">退出</el-menu-item>
    </el-sub-menu>
  </el-menu>
</template>

<script lang="ts" setup>
import { ref, computed } from "vue";
import { Calendar, Search } from "@element-plus/icons-vue";
const searchText = ref("");
</script>

<style lang="scss" scoped>
.logo {
  width: 180px;
  height: 59px;
  background-image: url("~@/assets/logo.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

.title {
  font-size: 24px;
  font-weight: bold;
  color: #333;
  margin-left: 10px;
}

.div-separator {
  width: 1px;
  height: 80%; /* 分割线的高度 */
  background-color: #ccc; /* 分割线的颜色 */
  margin: 0 auto; /* 水平居中 */
}

.flex-grow {
  flex-grow: 1;
}

.serach-input {
  width: 160px;
  margin: 10px;
  //圆角
  border-radius: 20px;
  //边框
  border: 1px solid #ccc;
  //字体大小
  font-size: 18px;
  //字体颜色
  color: #333;
  //输入框内文字居中
  text-align: center;
  //输入框内文字垂直居中
  display: flex;
  //字体加粗
  font-weight: bold;

  align-items: center;
  //输入框内文字水平居中
  justify-content: center;
  //输入框内边距
  padding: 0 10px;
  //输入框内图标
}

:deep(.el-input__wrapper) {
  box-shadow: 0 0 0 0px var(--el-input-border-color, var(--el-border-color))
    inset;
  cursor: default;
  border: none !important;
}
</style>