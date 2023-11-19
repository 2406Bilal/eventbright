<script setup>
import { Heart, Upload, CalendarSearch, Youtube, Twitter, Flag, Globe } from 'lucide-vue-next';
</script>

<template>
    <div class="mx-auto bg-[url('/assets/img/background.png')] mt-8 bg-no-repeat bg-center rounded-xl flex justify-center items-center w-full">
        <img src="~/assets/img/first.png" class="mx-auto" alt="">
    </div>
    <div class="flex flex-col lg:flex-row max-w-[1200px] m-auto mt-7 p-3">
        <div 
        class="max-w-[720px] mt-12">
           <p 
            class="text-lg leading-6 font-semibold">
                Wednesday, November 15
            </p>
            <div class="text-5xl font-extrabold space-y-5 mt-4">
                <p> 
                    Machine Learning Platform</p>
                   <p>for Anti Money Laundering
                </p> 
             </div> 
             <div class="text-sm font-bold leading-6 text-Darkblue mt-12">
                <p>
                    Get ready to explore the ultimate Machine Learning Platform for Anti Money Laundering, where we'll unravel combating money laundering
                </p>
            </div>
            <div>
                <UiCard
                class="grid grid-cols-3 gap-4 place-items-center rounded-xl border-transparent bg-slate-100 w-full h-22 mt-6  lg:py-4 px-6"> 
                        <UiCardHeader
                        class="flex flex-row w-52  p-0 space-x-4">
                            <UiAvatar 
                            size="base"
                            class="self-center">
                                <UiAvatarImage src="https://fastly.picsum.photos/id/370/500/500.jpg?hmac=FZVTASfmfretWcWn30Qfv-IUd6N0DkBggbEsvV6zsWw"/>
                            </UiAvatar>
                            <p
                            class="space-x-10 text-sm font-normal">by
                            <span class="text-base font-semibold">KAt Usap, MSHI</span><br>14,2 followers</p>
                        </UiCardHeader>
                    <UiCardFooter
                    class="">
                        <UiButton
                        class="bg-sky-700 w-28 h-11 rounded self-center mt-6">
                            <p
                            class="text-white">Follow</p>
                        </UiButton>
                    </UiCardFooter>
                </UiCard>
            </div>
            <div>
                <p
                class="text-2xl font-bold mt-12">
                    Date and time
                </p>
                <div
                class="mt-3 flex items-stretch">
                    <div class="flex flex-row">
                        <div 
                        class="w-6 h-6">
                            <CalendarSearch />
                        </div>
                        <p
                        class="text-sm font-normal self-center ml-4">
                            Wednesday, November 15 · 2 - 3pm UTC
                        </p>
                    </div>   
                </div>        
            </div> 
            <div 
             class="mt-20">
             <p
             class="text-2xl font-bold leading-7">location</p>
                <div 
                class="flex items-stretch mt-4">
                    <div class="flex flex-row">
                        <div
                        class="w-6 h-6"> 
                            <Youtube/>
                        </div>
                        <p 
                        class="text-sm font-semibold leading-5 ml-4">
                            Online
                        </p>
                    </div>
                </div>
                <div>
                    <p
                    class="text-2xl font-bold leading-7 mt-14">
                        Agenda
                    </p>
                </div>
                <div
                class="w-full mt-4">
                        <div class="p-4 rounded-xl bg-bg1 mt-4">
                            <div
                            class="border-l-4 bg-bg1">
                                <p class="text-sm font-semibold leading-5 ml-4">9:00 AM-9:20 AM</p>
                                <p class="text-lg font-semibold leading-6 ml-4">Intro to Machine Learning Platform for Anti Money Laundering</p>
                            </div>
                        </div>
                    <div class="p-4 rounded-xl bg-bg2 mt-4">
                        <div
                        class="border-l-4">
                            <p class="text-sm font-semibold leading-5 ml-4">9:20 AM-9:40 AM</p>
                            <p class="text-lg font-semibold leading-6 ml-4">Demo: Machine Learning Platform for Anti Money Laundering</p>  
                        </div>
                    </div>
                    <div class="p-4 rounded-xl bg-bg3 mt-4">
                        <div
                        class="border-l-4">
                            <p class="text-sm font-semibold leading-5 ml-4">9:40 AM-10:55 AM</p>
                            <p class="text-lg font-semibold leading-6 ml-4">Q&A</p>
                        </div>
                    </div>
                    <div class="p-4 rounded-xl bg-bg4 mt-4">
                        <div
                        class="border-l-4">
                            <p class="text-sm font-semibold leading-5 ml-4">"9:55 AM-10:00 AM</p>
                            <p class="text-lg font-semibold leading-6 ml-4">Closing Remarks</p>  
                        </div>
                    </div>
                </div>

                <div class="text-2xl font-bold leading-7 mt-12">
                    <p>About this event</p>
                </div>
                <div>
                    <div 
                    class="text-sm font-semibold leading-5 flex flex-row mt-7">
                        <p 
                        class="ml-12">
                            1 hour
                        </p>
                        <p class="ml-52">
                            Mobile eTicket
                        </p>
                    </div>
                    <div 
                    class="w-full mt-9">
                        <p
                        class="text-base font-bold leading-6">Machine Learning Platform for Anti Money Laundering</p>
                        <div
                        class="text-base font-normal leading-6">
                            <p class="mt-3">Join us for an exciting online event where we delve into the world of machine learning and its vital role in combating money laundering.</p>
                            <p class="mt-3">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Itaque hic facere architecto? Laudantium assumenda expedita, repudiandae dignissimos, at sapiente consequatur quis tenetur iusto dolorum sequi, placeat quam labore aliquam necessitatibus!Lorem</p>
                            <p class="mt-3">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perspiciatis quod nesciunt, laborum facilis necessitatibus perferendis vitae est mollitia sapiente vero possimus non totam repellendus rem suscipit reiciendis, amet quo distinctio. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet eligendi modi eos. Doloribus non earum aut nisi omnis vitae voluptatem maiores alias minima inventore? Voluptatem dolor possimus nihil. Necessitatibus, inventore.
                            </p>
                        </div>
                    </div>
                    <!-- organization card -->
                    <div>
                        <div
                        class="font-bold mt-2">
                            About the organization
                        </div>
                        <!-- card-->
                        <div
                        class="shadow-2xl mt-3">
                            <UiCard
                            class="grid justify-items-center border-transparent rounded-xl">
                                <UiCardHeader
                                class="mt-10">
                                    <UiAvatar
                                    size="base">
                                        <img src="https://picsum.photos/500/500" alt="">
                                    </UiAvatar>
                                </UiCardHeader>
                                <UiCardContent
                                class="text-center">
                                    <p 
                                    class=" text-sm font-normal leading-5 text-org mt-8 text-center">Organized by</p>
                                    <a href="#"
                                    class="text-xl font-semibold leading-6 mt-2 hover:text-blue-700 hover:underline">Hopswork</a>
                                    <p
                                    class="text-xl font-bold leading-7 mt-6">43</p>
                                    <p 
                                    class="text-sm font-normal leading-5 text-org text-center">followers</p>
                                    <div>
                                        <div
                                        class=" flex flex-row tems-center">
                                        <UiButton 
                                                class="bg-slate-50 hover:bg-slate-100 w-28 h-11 rounded self-center mt-6">
                                                <p 
                                                class="text-textli font-semibold text-sm">Contact</p>
                                        </UiButton> 
                                        <div 
                                        class="ml-4">
                                            <UiButton 
                                                class="bg-sky-700 w-28 h-11 rounded self-center mt-6">
                                                    <p 
                                                    class="text-white font-semibold text-sm">Follow</p>
                                            </UiButton>    
                                        </div>
                                        </div>
                                    </div>
                                </UiCardContent>
                                <UiCardFooter
                                class="flex flex-row">
                                    <div
                                    class="p-3 text-textli bg-bgicon rounded-xl">
                                        <Twitter />
                                    </div>
                                    <div
                                    class="p-3 ml-11 text-textli bg-bgicon rounded-xl">
                                        <Globe /> 
                                    </div>
                                </UiCardFooter>
                            </UiCard>
                        </div>
                    </div>
                    <div
                    class="grid justify-items-center text-textli mt-14">
                        <div
                        class="flex flex-row">
                            <div>
                                <Flag />
                            </div>
                            <p 
                            class="text-sm font-semibold leading-5 ml-3">report this even</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- card -->
        <div class="w-full lg:w-[360px] mt-12 flex flex-col">
            <div class=" flex justify-end flex-row h-12 w-full">
                <div 
                class="ml-2">
                    <Heart />
                </div>
                <div
                class="ml-4">
                    <Upload />
                </div>
            </div> 
            <div class="fixed bottom-0 left-0 w-full  lg:left-auto lg:bottom-auto mr-1 ml-2 lg:sticky lg:top-10 lg:z-10 lg:rounded lg:mr-1 lg:ml-2">
                <UiCard 
                class=" lg:sticky lg:top-10 lg:z-10 lg:rounded-xl -ml-2 lg:mr-1 lg:ml-2 border-inherit srounded-none">
                    <UiCardHeader>
                        <UiCardHeader
                        class="-mt-4">
                           <p
                           class="text-xl font-semibold h-2 text-center"> 
                            $99.99</p> 
                        </UiCardHeader>
                    </UiCardHeader>
                    <UiCardFooter 
                    class="-mt-4">
                        <Button class="w-full h-9 rounded bg-oran">
                          <p
                          class="text-base font-semibold text-white">
                          Tickets</p>
                        </Button>
                    </UiCardFooter>
                </UiCard>
            </div>
        </div>
    </div>
</template>