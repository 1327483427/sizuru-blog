<template>
  <div class="common-layout">
    <el-container>
      <el-header>
        <el-row style="text-align: center; min-height: 60px">
          <el-col :span="4">
            <el-image class="brandArea" :src="favicon" :fit="fit"></el-image>
          </el-col>

          <el-col :span="18">
            <el-menu
              router="router"
              :default-active="activeIndex"
              :active-text-color="activeColor"
              class="el-menu-demo"
              style="position: static"
              mode="horizontal"
              @select="handleSelect"
            >
              <el-row>
                <el-col :span="4">
                  <el-submenu index="/blog">
                    <template slot="title">博客</template>
                    <el-menu-item index="/blog/blogMain">首页</el-menu-item>
                    <el-menu-item index="/blog/blogSelf">我的</el-menu-item>
                  </el-submenu>
                </el-col>
                <el-col :span="4">
                  <el-menu-item index="2">音乐</el-menu-item>
                </el-col>
                <el-col :span="4">
                  <el-menu-item index="3" disabled>视频</el-menu-item>
                </el-col>
                <el-col :span="4">
                  <el-menu-item index="4">游戏</el-menu-item>
                </el-col>
                <el-col :span="4">
                  <el-menu-item index="5">社区</el-menu-item>
                </el-col>
              </el-row>
            </el-menu>
          </el-col>
          <el-col :span="2">
            <el-image class="headArea" :src="headImg" :fit="fit"></el-image>
          </el-col>
        </el-row>
      </el-header>
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-container>
          <el-main>Main</el-main>
          <el-footer>Footer</el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<script lang="ts">
export default {
  name: "Index",
};
</script>

<style scoped>
.el-header {
  background-color: #f1f4f8;
  height: 70px;
}
</style>
