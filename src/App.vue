<!--
 * @Author: yutaiqi
 * @Date: 2024-01-11 21:45:54
 * @LastEditTime: 2024-01-28 15:04:11
 * @LastEditors: yutaiqi
 * @Description: 文件功能描述
 * @FilePath: /sytstudy/src/App.vue
-->
<script setup lang="ts">
import useUserInfoStore from '@/store/modules/userInfo'
const userInfoStore = useUserInfoStore()
</script>

<template>
    <div class="container">
        <!-- 头部区域 -->
        <HospitalTop/>
 
        <!-- 内容区域 -->
        <div class="content">
           <!-- 路由组件 -->
            <router-view />
        </div>

        <!-- 底部区域 -->
        <HospitalBottom/>

        <!-- 登录弹窗  -->
        <Login :visible="userInfoStore.loginVisible" />

    </div>
</template>

<style scoped lang="scss">
.container{
    display: flex;
    flex-direction: column;
    align-items: center;

    .content{
        width: 1200px;
        min-height: calc(100vh - 120px);
    }
}
</style>
