<template>
    <div class=" fixed top-[0%] bg-black text-[#f1f1f1] z-30 w-full">
        <div class="container flex flex-col lg:flex-row justify-start lg:justify-between items-start lg:items-center">
            <div class="text-xl uppercase lg:-skew-y-12 text-orange-500 font-semibold  bg-white px-2 drop-shadow-md shadow-md shadow-orange-5">
                our world
            </div>
            <div :class="showMenu" >
                <ul class="flex flex-col lg:flex-row justify-start lg:justify-center items-start lg:items-center">
                    <a 
                       href="#"
                       v-for="nav in navEl" :key="nav.id" 
                       class="py-5 w-full lg:w-auto px-5 font-semibold text-lg capitalize hover:bg-orange-500 transition-all ease-in-out duration-300"
                    >
                        {{ nav.navName }}
                    </a>
                </ul>
            </div>
            <div class="block lg:hidden" >
                <span><i @click="toggleMenu" class='bx bx-menu'></i></span>
            </div>
        </div>
    </div>
</template>

<script setup>
 import { ref } from 'vue';

 const navEl = ref([
    {
        navName : 'Home',
        id: 1,
        url: '#home'
    },
    
    {
        navName : 'about us',
        id: 2,
        url: '#about'
    },

    {
        navName : 'profile',
        id: 3,
        url: '#profile'
    },

    {
        navName : 'application',
        id: 4,
        url: '#application'
    },

    {
        navName : 'company',
        id: 5,
        url: '#company'
    },

    {
        navName : 'contact',
        id: 6,
        url: '#contact'
    }
 ]);

 const showMenu = ref(false);
 const toggleMenu = () =>{
     showMenu.value =!showMenu.value;
 }
</script>