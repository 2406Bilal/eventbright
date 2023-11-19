<template>
    <div class="bg-slate-100">
     <div class="flex flex-col">
      <img  src="~/assets/img/card.png" class="w-full" alt="" />
      <div class="py-2 px-4">
        <h3 class="text-xl text-primary-dark-1 font-semibold pt-4">
          machine Learning platform
        </h3>
        <p class="text-primary-grey-2 font-semibold">20.February</p>
        <p v-if="card.price" class="text-primary-dark-1 font-semibold">
          From $20.00
        </p>
        <p v-else class="text-primary-dark-1 font-semibold">
          Check ticket price on event
        </p>
      </div>
     </div>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    card: Object,
  });
  
  console.log(props.card.img);
  </script>
