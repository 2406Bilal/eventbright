<script setup>
import { ref, watch } from 'vue';
import {
    Select,
    SelectContent,
    SelectGroup,
    SelectItem,
    SelectTrigger,
    SelectValue,
} from '@/components/ui/select';

const countryCode = ref('');
const phoneNumber = ref('');
const agreeTerms = ref(false);
const isButtonDisabled = ref(true);

const changeButtonState = () => {
    if (countryCode.value.length > 0 && phoneNumber.value !== null && agreeTerms.value === true) {
        isButtonDisabled.value = false;   
    } else {
        isButtonDisabled.value = true;   
    }
};

const handleButtonClick = () => {
    console.log("Country Code:", countryCode.value);
    console.log("Phone Number:", phoneNumber.value);
    console.log("Agree Terms:", agreeTerms.value);
    countryCode.value = '';
    phoneNumber.value = '';
    agreeTerms.value = false;
};

watch(countryCode, () => {
    changeButtonState();
});

watch(phoneNumber, () => {
    changeButtonState();
});

watch(agreeTerms, () => {
    changeButtonState();
});

const countryCodeCheck = [
    {
        id: 111,
        name: "Russia",
        value: '+7'
    },
    {
        id: 222,
        value: '+77',
        name: "Korea"
    },
    {
        id: 333,
        value: '+88',
        name: "China"
    },
    {
        id: 444,
        value: '+99',
        name: "Tajikistan"
    },
    {
        id: 555,
        value: '+1',
        name: "USA"
    }    
];
</script>
<template>
    <div class="lg:flex">
        <div class="lg:w-3/5 p-16">
            <div class="text-4xl font-bold space-y-3">
                <h1>First, we'll send you a code to verify it's you</h1>
            </div>
            <div class="text-base font-semibold mt-4">
                <p>Eventbrite is a place to find real events. We ask organizers for their phone number so we can verify their identity, secure their account, and keep our community safe.</p>
                <p class="mt-4">We'll send a one-time verification code to the number you provide.</p>
            </div>
            <div class="flex flex-col lg:flex-row mt-4 space-y-3 border-black lg:p-3 items-center w-full">
                <Select v-model="countryCode" :class="{ 'border-red-500': isButtonDisabled }">                
                    <SelectTrigger class="border-black rounded-xl h-12 lg:w-40">
                    <SelectValue placeholder="Country" />
                    </SelectTrigger>
                    <SelectContent>
                        <SelectGroup>
                            <SelectItem v-for="item in countryCodeCheck" :key="item.id" :value="item.value">{{ item.name}}</SelectItem>
                        </SelectGroup>
                    </SelectContent>
                </Select>
                <div class="lg:w-96 w-full">
                    <UiInput
                    v-model="phoneNumber"
                    class="focus:border-black w-full lg:ml-3 h-12 placeholder:text-black lg:-mt-3 border-black rounded-xl"
                    type="number"
                    placeholder="Phone number"
                    :class="{ 'border-red-500': phoneNumber.length === 0 }"
                />
              </div>
            </div>
            <div class="flex flex-row items-center mt-4">
                <div class="mr-3">
                    <input type="checkbox" id="terms" v-model="agreeTerms">
                    <!-- <Checkbox id="terms" v-model="agreeTerms" />  -->
                </div>
                <div>
                    <label
                        for="terms"
                        class="text-sm font-medium leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70 space-y-0"
                    >
                        I agree to Eventbrite's SMS Terms of Service and Privacy Policy and consent to receive a verification text message from Eventbrite. Message and data rates may apply.
                    </label>
                </div>
            </div>
            <div class="border-black mt-8">
                <UiButton
                @click="handleButtonClick"
                :disabled="isButtonDisabled"
                class="focus:bg-slate-500 rounded-xl"
                :class="{ 'bg-red-500': isButtonDisabled, 'focus:bg-slate-500': !isButtonDisabled }"
            >
                <p class="text-black">Send code</p>
            </UiButton>
            </div>
        </div>
        <!-- photo -->
        <div class="lg:w-2/5 hidden lg:block">
            <img src="~/assets/img/bgAdd.svg" class="w-full" alt="">
        </div>
    </div>
</template>
