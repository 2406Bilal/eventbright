<script setup>
import { ref } from 'vue';
const showError = ref('');
const email = ref('');
const login = () => {
  if (email.value.trim() === '') {
    showError.value = true;
    return;
  }
  console.log('Email:', email.value);
  email.value = '';
}
</script>
<template>
  <div class="lg:flex">
    <div class="lg:w-1/2 lg:p-6">
      <div class="lg:w-96 mx-auto">
        <div class="w-full py-6 px-6 mt-[90px]">
          <div>
            <img src="~/assets/icons/logo.svg" alt="" />
          </div>
          <div class="flex flex-row mt-6 justify-between">
            <p class="text-4xl font-extrabold">Create an account</p>
            <NuxtLink to="#" class="text-sky-600 justify-items-end"
              >Log in</NuxtLink
            >
          </div>
          <div class="w-full mt-6 space-y-2">
            <UiInput
              type="email"
              required
              placeholder="Email address"
              :class="{ 'border-red-500': showError }"
              v-model='email'
            />
            <p v-if="showError" class="text-red-500 mt-2">
              Please enter a valid email address
            </p>
          </div>
        </div>
        <div class="p-5">
          <UiButton @click="login" class="w-full bg-oran focus:bg-oran">
            <p>Log in</p>
          </UiButton>
        </div>
        <div class="flex flex-col space-y-3 p-5">
          <UiButton class="h-12 bg-white text-black border focus:bg-white">
            Email me a login link
          </UiButton>
        </div>
        <div class="p-5">
          <p>Other login methods</p>
          <div class="flex flex-row mt-5">
            <a href="#">
              <img src="~/assets/icons/facebook → SVG.svg" alt=" "/>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="lg:w-1/2 hidden lg:block">
      <div class="">
        <img
          src="~/assets/img/signIn.png"
          alt=""
          class="w-full h-full"/>
      </div>
    </div>
  </div>
</template>