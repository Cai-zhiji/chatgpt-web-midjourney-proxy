<script setup lang="ts">
import { NAlert, NDataTable } from 'naive-ui'

const modelPricing = [
  { model: 'pt-3.5-turbo', price: '2积分/次' },
  { model: 'gpt-4-turbo-2024-04-09', price: '10积分/次' },
  { model: 'gpt-4o', price: '10积分/次' },
  { model: 'claude-3-sonnet-20240229', price: '10积分/次' },
  { model: 'gemini-pro', price: '10积分/次' },
  { model: 'kimi', price: '10积分/次' },
  { model: 'glm-4', price: '10积分/次' },
  { model: 'gpt-4-vision-preview', price: '30积分/次' },
  { model: 'midjourney', price: '40积分/次' },
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
    由于gpt-4-all模型是逆向模型，有时可能识别不到文件内容，如出现这种情况，联系客服可退还相应积分。
  </NAlert>
  <div class="max-w-4xl mx-auto mt   p-5 bg-white rounded shadow">
    <NDataTable :columns="columns" :data="modelPricing" :single-line="false" bordered class="text-gray-700" />
  </div>
</template>

<style scoped>
@import 'https://cdn.jsdelivr.net/npm/tailwindcss@^2.0/dist/tailwind.min.css';

div {
  @apply text-sm sm:text-base;
}
</style>
