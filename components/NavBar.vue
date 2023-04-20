<template>
  <div class="navbar">
    <div class="container flex items-center h-[60px]">
      <n-button text class="text-xl font-bold">米谷教育</n-button>
      <ui-menu>
        <ui-menu-item v-for="(item, index) in menus" :key="index" :active="(route.path === item.path)"
          @click="handleOpen(item.path)">
          {{ item.name }}
        </ui-menu-item>
      </ui-menu>
      <n-button circle class="ml-auto mr-5">
        <template #icon>
          <n-icon>
            <Search />
          </n-icon>
        </template>
      </n-button>
      <!-- <n-button strong secondary>登录</n-button> -->
      <n-dropdown :options="userOptions">
        <n-avatar round size="small" src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg" />
      </n-dropdown>
    </div>
  </div>
  <div class="w-[100%] h-[80px]">

  </div>
</template>

<script setup lang="ts">
import { useRoute, useRouter } from 'vue-router'
import { NButton, NIcon, NDropdown, NAvatar } from 'naive-ui';
import { Search } from '@vicons/ionicons5'
import { userOptionsType, menuType } from '@/type/navBar-type'

// 获取路由地址
const route = useRoute()

// 获取路由对象
const router = useRouter()

const userOptions = ref<userOptionsType[]>([
  {
    label: '用户资料',
    key: 'center'
  },
  {
    label: '退出',
    key: 'logout'
  }
])


const menus = ref<menuType[]>([
  {
    name: '首页',
    path: '/',
  },
  {
    name: '考试',
    path: '/paper/1',
    match:[
      {
        name:'paper-page'
      }
    ]
    
  },
  {
    name: '拼团',
    path: '/list/group/1'
  },
  {
    name: '秒杀',
    path: '/list/flashsale/1'
  },
  {
    name: '直播',
    path: '/list/live/1'
  },
  {
    name: '专栏',
    path: '/list/column/1'
  },
  {
    name: '电子书',
    path: '/list/book/1'
  },
  {
    name: '社区',
    path: '/list/bbs/1'
  },
  {
    name: '课程',
    path: '/list/course/1'
  }
])


const handleOpen = (path: string) => {
  navigateTo(path)
}
</script>

<style>
.navbar {
  z-index: 1000;
  @apply bg-white fixed top-0 left-0 right-0 shadow-sm;
}
</style>