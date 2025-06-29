<script setup lang="ts">
defineProps({
  modelValue: {
    type: String,
    required: true
  },
  placeholder: {
    type: String,
    default: 'Please Enter'
  }
});

defineEmits(['update:modelValue']);
</script>

<template>
  <div class="relative rounded bg-white w-full flex items-start gap-[10px]">
    <input
      :value="modelValue"
      @input="$emit('update:modelValue', ($event.target as HTMLInputElement).value)"
      :placeholder="placeholder"
      class="box-border w-full px-[16px] py-[8px] rounded-[4px] border border-solid border-[#DCDFE6] bg-[#fff] font-['Helvetica_Neue',_sans-serif] text-[14px] text-black placeholder:text-[#c0c4cc] focus:outline-none focus:border-[#E6A23C] focus:shadow-[0px_0px_0px_2px_#f8e3c5]"
    />
  </div>
</template>

<style scoped>
/* Component-specific styles can go here if needed */
</style>
