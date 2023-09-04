<template>
  <div class="index-page">
    <a-input-search
        v-model:value="searchText"
        placeholder="请输入搜索关键词"
        enter-button="搜索"
        size="large"
        @search="onSearch"
    />
    <MyDivider />
    <a-tabs v-model:activeKey="activeKey" @change="onTabChange">
      <a-tab-pane key="post" tab="文章">
        <PostList :post-list="postList" />
      </a-tab-pane>
      <a-tab-pane key="picture" tab="图片">
        <PictureList :picture-list="pictureList" />
      </a-tab-pane>
      <a-tab-pane key="user" tab="用户">
        <UserList :user-list="userList" />
      </a-tab-pane>
    </a-tabs>
  </div>
</template>

<script lang="ts">
import MyDivider from "@/components/MyDivider.vue";
</script>
