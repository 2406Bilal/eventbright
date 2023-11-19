<template>
  <div>
    <header
      class="flex justify-between items-center px-3 py-6 gap-4 sm:gap-14 lg:gap-0 lg:px-6"
    >
      <div class="flex items-center gap-4 w-full lg:w-96">
        <NuxtLink to="/">
          <img
            class="sm:hidden"
            src="../assets/icons/mobile-logo.svg"
            alt="logo"
          />
          <img
            class="hidden sm:block"
            src="../assets/icons/logo.svg"
            alt="logo"
          />
        </NuxtLink>
        <UiButton
          class="flex justify-start bg-primary-grey-1 text-primary-dark-1 text-xs p-3 w-full rounded-3xl border hover:bg-inherit sm:text-sm"
          ><img src="../assets/icons/search.svg" alt="search" class="mr-1" />
          Search</UiButton
        >
      </div>

      <nav class="mr-8 lg:mr-0">
        <ul class="flex gap-3 text-xs sm:text-sm lg:hidden">
          <li class="shrink-0"><NuxtLink to="/auth/login">Log In</NuxtLink></li>
          <li class="shrink-0"><NuxtLink to="/auth/register">Sign Up</NuxtLink></li>
        </ul>
        <ul
          class="hidden lg:flex items-center gap-10 font-semibold text-sm text-primary-dark-1"
        >
          <li>Find Events</li>
          <li><NuxtLink to="/addevents/addevent">Create Events</NuxtLink></li>
          <li>Help Center</li>
          <li><NuxtLink to="/auth/login">Log In</NuxtLink></li>
          <li><NuxtLink to="/auth/register">Sign Up</NuxtLink></li>
        </ul>
      </nav>
      <Sheet>
        <SheetTrigger as-child class="lg:hidden">
          <button><Menu /></button>
        </SheetTrigger>
        <SheetContent>
          <ul>
            <li>Find Events</li>
            <li> <a href="../pages/addevents/addevents.vue">Create Events</a></li>
            <li>Help Center</li>
          </ul>
        </SheetContent>
      </Sheet>
    </header>

    <div>
      <slot />
    </div>
    <footer class="bg-[#1E0A3C] pt-7 pb-7 px-6">
      <div class="flex justify-center gap-1">
        <img src="../assets/icons/footer-icon.svg" alt="" />
        <span class="text-[#6F7287]">|</span>
        <img src="../assets/icons/footer-logo.svg" alt="footer logo" />
      </div>

      <div
        class="flex flex-col gap-10 items-center mt-16 md:flex-row lg:gap-5 lg:justify-between"
      >
        <p class="text-white text-xs">© 2023 Eventbrite</p>

        <nav>
          <ul
            class="flex flex-col flex-wrap items-center gap-4 text-white text-xs md:flex-row md:justify-center lg"
          >
            <li>About</li>
            <li>Blog</li>
            <li>Help</li>
            <li>Careers</li>
            <li>Press</li>
            <li>Impact</li>
            <li>Investors</li>
            <li>Security</li>
            <li>Developers</li>
            <li>Terms</li>
            <li>Privacy</li>
            <li>Security</li>
            <li>Developers</li>
            <li>Terms</li>
            <li>Privacy</li>
            <li>CA Privacy Notice</li>
            <li>Accessibility</li>
            <li>Cookies</li>
            <li>Manage Cookie Preferences</li>
          </ul>
        </nav>

        <p class="text-white text-xs">Tajikistan</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { Menu } from "lucide-vue-next";

import { Button } from "@/components/ui/button";
import {
  Sheet,
  SheetClose,
  SheetContent,
  SheetDescription,
  SheetFooter,
  SheetHeader,
  SheetTitle,
  SheetTrigger,
} from "@/components/ui/sheet";
</script>

<style></style>