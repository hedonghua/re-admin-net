<template>
    <div>
        <div class="re-card">
            <el-descriptions title="项目信息" column="1">
                <el-descriptions-item label="名称">{{ APP_TITLE }}</el-descriptions-item>
                <el-descriptions-item
                    label="概述">使用Vite+Vue构建，使用了许多热门框架和技术，如：element-plus,axios,tailwindcss,pinia等</el-descriptions-item>
                <el-descriptions-item label="背景">想写一款后台管理框架，这是我一直想做的事，用于开源和自己接单做项目</el-descriptions-item>
            </el-descriptions>

            <el-descriptions title="仓库信息" column="1" class="mt-2">
                <el-descriptions-item label="Github">https://github.com/hedonghua/re-admin</el-descriptions-item>
            </el-descriptions>

            <el-descriptions title="联系作者" column="1" class="mt-2">
                <el-descriptions-item label="邮箱">crackerwork@outlook.com</el-descriptions-item>
            </el-descriptions>
        </div>

        <el-row :gutter="20" class="mt-3">
            <el-col :span="12">
                <div class="re-card">
                    <h2 class="el-descriptions__title">更新日志</h2>
                    <el-collapse accordion class="mt-4">
                        <el-collapse-item title="v1.0.0" name="v1.0.0">
                            <div>
                                基本功能稳定
                            </div>
                        </el-collapse-item>
                    </el-collapse>
                </div>
            </el-col>
            <el-col :span="12">
                <div class="re-card">
                    <h2 class="el-descriptions__title">捐赠支持</h2>
                    <div class="mt-4 flex">
                        <div class="text-center">
                            <p>微信</p>
                            <re-image width="150px" height="150px" :src='WxPay' :previewList='[WxPay]' fit="cover" />
                        </div>
                        <div class="text-center ml-5">
                            <p>支付宝</p>
                            <re-image width="150px" height="150px" :src='AliPay' :previewList='[AliPay]' fit="cover" />
                        </div>
                    </div>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue';
import WxPay from '@/assets/img/wxpay.jpg';
import AliPay from '@/assets/img/alipay.jpg';

const APP_TITLE = import.meta.env.VITE_APP_TITLE;

onMounted(() => {
})
</script>