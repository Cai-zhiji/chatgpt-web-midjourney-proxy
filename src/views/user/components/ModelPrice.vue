<script setup lang="ts">
import { NAlert, NDataTable } from 'naive-ui'

const modelPricing = [
  { model: 'gpt-3.5-turobo', price: '免费' },
  { model: 'gpt-3.5-turobo-16k', price: '0积分/次（限时免费）' },
  { model: 'gpt-4-0125-preview', price: '10积分/次' },
  { model: 'gpt-4-turbo-preview', price: '10积分/次' },
  { model: 'gpt-4-vision-preview', price: '30积分/次' },
  { model: 'gpt-4-all', price: '50积分/次' },
  { model: 'midjourney', price: '50积分/次' },
]

const columns = [
  {
    title: '模型名称',
    key: 'model',
  },
  {
    title: '定价',
    key: 'price',
  },
]
</script>

<template>
  <NAlert type="warning" closable>
    本站提供ChatGPT官网GPT4代充服务，详细信息添加客服微信了解更多：ACGWAQT
  </NAlert>
  <div class="max-w-4xl mx-auto mt   p-5 bg-white rounded shadow">
    <NDataTable
      :columns="columns"
      :data="modelPricing"
      :single-line="false"
      bordered
      class="text-gray-700"
    />
  </div>
</template>

<style scoped>
@import 'https://cdn.jsdelivr.net/npm/tailwindcss@^2.0/dist/tailwind.min.css';

div {
  @apply text-sm sm:text-base;
}
</style>
