<script setup lang="ts">
import { NAlert, NDataTable } from 'naive-ui'

const modelPricing = [
  { model: 'gpt-3.5-turbo-0125', price: '免费' },
  { model: 'gpt-4-0125-preview', price: '10积分/次' },
  { model: 'gpt-4-vision-preview', price: '30积分/次' },
  { model: 'gpt-4-all', price: '40积分/次' },
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
