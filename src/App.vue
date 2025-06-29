<script setup lang="ts">
import { ref } from 'vue';
import InputField from './components/InputField.vue';
import StatusTag from './components/StatusTag.vue';

const inputValue = ref('');
</script>

<template>
  <div class="flex flex-col min-h-screen w-full items-center justify-center px-6 sm:p-[16px] md:p-[24px] lg:p-[32px]">
    <div class="w-full max-w-[640px] mx-auto text-center flex flex-col items-center">
    <h1 class="text-2xl sm:text-3xl font-bold text-blue-500">Vue3 Components</h1>
    <div class="w-20 h-6 bg-gray-300 my-4"></div>
    <div class="w-full flex flex-col items-center mb-[16px]">
      <h1 class="text-2xl sm:text-3xl font-bold text-blue-500">Input Field</h1>
      <InputField v-model="inputValue" />
    </div>
    <div class="p-6 rounded-lg shadow w-full">
      <h1 class="text-2xl sm:text-3xl font-bold text-blue-500">Status Tag</h1>
      <div class="flex gap-[16px] justify-center">
        <StatusTag status="active" />
        <StatusTag status="inactive" />
        <StatusTag status="pending" />
        <StatusTag status="error" />
      </div>
    </div>
  </div>
</div>
</template>