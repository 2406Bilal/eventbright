<template>
    <div>
      <div class="flex flex-col items-center gap-2 cursor-pointer">
        <div
          class="flex justify-center items-center border border-[#DEE5FF] rounded-full bg-white p-4 sm:p-8"
        >
          <slot />
        </div>
        <p class="text-xs font-semibold">{{ name }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    name: String,
  });
  </script>
  cat