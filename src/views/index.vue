<template>
  <div class="common-layout">
    <el-container>
      <el-header>
        <blog-header />
      </el-header>
      <el-container>
        <el-aside width="200px">
          <blog-aside />
        </el-aside>
        <el-container>
          <el-main>
            <blog-main />
          </el-main>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<script lang="ts" setup>
import BlogHeader from "../components/BlogHeader.vue";
import BlogMain from "../components/BlogMain.vue";
</script>

<style>
.flex-grow {
  flex-grow: 1;
}
</style>