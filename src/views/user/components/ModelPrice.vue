<script setup lang="ts">
import { NDataTable } from 'naive-ui'

const modelPricing = [
  { model: 'gpt-3.5-turobo', price: '免费' },
  { model: 'gpt-3.5-turobo-16k', price: '限时免费' },
  { model: '示例模型1', price: '$19.99' },
  { model: '示例模型2', price: '$29.99' },
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
