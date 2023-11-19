<template>
    <div>
      <main>
        <section
          class=""
        >
        <img src="~/assets/img/firstA.png" class="-mt-7 h-full" alt="">
          <UiButton class="py-3 px-4 bg-dark-orange-1 font-semibold"
            >Find your next event</UiButton
          >
        </section>
  
        <section
          class="flex flex-wrap justify-center bg-primary-grey-1 px-7 py-5 gap-x-5 gap-y-7 sm:flex-nowrap sm:gap-14 sm:overflow-scroll sm:justify-start lg:justify-center lg:py-9"
        >
          <Category name="Music">
            <Mic2 class="text-[#627DEB] sm:text-primary-dark-1  hover:text-primary-blue transition-colors ease-in-out" />
          </Category>
          <Category name="Nightlife">
            <Club class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Performing ">
            <Drama class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Holidays">
            <CalendarHeart class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Health">
            <Stethoscope class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Hobbies">
            <Gamepad2 class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Business">
            <Presentation class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
          <Category name="Food & Drink">
            <Pizza class="text-[#627DEB] sm:text-primary-dark-1 hover:text-primary-blue transition-colors ease-in-out " />
          </Category>
        </section>
  
        <section class="py-10 border-b-8">
          <div class="container">
            <h2 class="text-3xl text-primary-dark-1 font-black">
              Popular in <span class="text-primary-blue">Tajikistan</span>
            </h2>
  
            <ul
              class="flex gap-4 text-primary-grey-2 mt-8 text-sm font-semibold overflow-scroll pb-2"
            >
              <li class="shrink-0 cursor-pointer text-primary-blue">All</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">For you</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Online</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Today</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">This weekend</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Veteran's Day</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Free</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Music</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Food & Drink</li>
              <li class="shrink-0 hover:text-primary-dark-1 transition-colors ease-in cursor-pointer">Charity & Causes</li>
            </ul>
  
            <h2 class="text-2xl font-bold text-primarylocalhost:3000-dark-1 mt-14">
              Events in Tajikistan
            </h2>
  
            <ul class="py-7 flex flex-wrap gap-4">
              <li
                v-for="card in cards"
                :key="card"
                class="hover:shadow-md transition-shadow ease-in-out rounded-xl grow lg:grow-0"
              >
                <NuxtLink to="/events/:id">
                  <Card :card="card" />
                </NuxtLink>
              </li>
            </ul>
            <div class="bg-primary-grey-1 py-8 pl-8">
                <h3 class="text-2xl text-primary-dark-1 font-bold">
                  Let's make it personal
                </h3>
                <p class="text-primary-grey-2">
                  Select your interests to get event suggestions based on what you
                  love
                </p>
                <Tags :interests="interests"/>
              </div>
            </div>
          </section>
    
          <section class="py-11">
            <div class="container">
              <h2 class="text-2xl text-primary-dark-1 font-bold">More events</h2>
    
              <ul class="py-7 flex flex-wrap gap-4">
                <li
                  v-for="card in cards"
                  :key="card"
                  class="hover:shadow-md transition-shadow ease-in-out rounded-xl grow lg:grow-0"
                >
                  <!-- <NuxtLink>
                    <Card :card="card" />
                  </NuxtLink> -->
                </li>
              </ul>
              <div class="flex justify-center">
                <UiButton
                  class="py-3 px-14 border-2 text-primary-dark-1 bg-white hover:bg-inherit font-semibold sm:px-24 md:px-32 lg:px-44"
                  >See more</UiButton
                >
              </div>
            </div>
          </section>
        </main>
      </div>
    </template>
    
    <script setup>
    import Category from "../components/category/category.vue";
    import Card from "../components/card/card.vue";
    // import Tags from "../components/tags/Tags.vue";
    
    import { Mic2 } from "lucide-vue-next";
    import { Club } from "lucide-vue-next";
    import { Drama } from "lucide-vue-next";
    import { CalendarHeart } from "lucide-vue-next";
    import { Stethoscope } from "lucide-vue-next";
    import { Gamepad2 } from "lucide-vue-next";
    import { Presentation } from "lucide-vue-next";
    import { Pizza } from "lucide-vue-next";
    import FlowImage from "~/assets/img/events/flow.jpg";
    
    const cards = reactive([
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
      {
        name: "8th Annual Goddess Flow",
        data: "Tomorrow • 2:00 PM",
        price: 20,
        img: FlowImage,
      },
    ]);
    
    const interests = reactive([
      "Comedy",
      "Food",
      "Education",
      "Pop",
      "Design",
      "Comedy",
      "Food",
      "Education",
      "Pop",
      "Design",
      "Comedy",
      "Food",
      "Education",
      "Pop",
      "Design",
      "Comedy",
      "Food",
      "Education",
      "Pop",
    ]);
    </script>
    
    <style lang="scss" scoped></style>