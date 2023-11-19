<script setup>
import { ref } from 'vue';

const email = ref('');
const password = ref('');
const showError = ref(false);
const passwordCheck = ref(false);

const login = () => {
  if (email.value.trim() === '' || password.value.trim() === '') {
    showError.value = true;
    return;
  }

  if (password.value.trim().length < 8) {
    passwordCheck.value = true
    return;
  }

  console.log('Email:', email.value);
  console.log('Password:', password.value);

  email.value = '';
  password.value = '';
  showError.value = false;
  passwordCheck.value= false;
}
</script>
<template>
  <div class="lg:flex">
    <div class="lg:w-1/2 lg:p-6">
      <div class="lg:w-96 mx-auto">
        <div class="w-full py-6 px-6 mt-[90px]">
          <div>
            <img src="~/assets/icons/logo.svg" alt=""/>
          </div>
          <div class="flex flex-row mt-6 justify-between">
            <p class="text-4xl font-extrabold">Log in</p>
            <NuxtLink to="#" class="text-sky-600 justify-items-end"
              >Sing up</NuxtLink
            >
          </div>
          <div class="w-full mt-6 space-y-2">
            <UiInput
              type="email"
              placeholder="Email address"
              :class="{ 'border-red-500': showError }"
              v-model='email'

            />
            <p v-if="showError" class="text-red-500 mt-2">
              Please enter a valid email address
            </p>
            <UiInput
              type="password"
              placeholder="Password"
              :class="{ 'border-red-500': showError }"
              v-model='password'
            />
            <p v-if="showError" class="text-red-500 mt-2">
              Please fill in all fields
            </p>
            <p v-if="passwordCheck" class="text-red-500 mt-2">
              your password have to be more that 8 charackters
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
          <UiButton class="h-12 bg-white text-black border focus:bg-white">
            Sign in with Google
          </UiButton>
        </div>
        <div class="p-5">
          <p>Other login methods</p>
          <div class="flex flex-row mt-5">
            <a href="#">
              <img src="~/assets/icons/facebook → SVG.svg" alt="" />
            </a>
            <a href="#">
              <img src="~/assets/icons/Button → SVG.svg" class="ml-6" alt="" />
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
          class="w-full h-[1080px]"
        />
      </div>
    </div>
  </div>
</template>
