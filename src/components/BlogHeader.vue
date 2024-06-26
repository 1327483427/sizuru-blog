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
      style="width: 200px"
      v-model="searchText"
      placeholder="请输入关键字"
      class="search-input"
    />
  </el-menu>
</template>

<script lang="ts" setup>
import { ref, computed } from "vue";
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
</style>