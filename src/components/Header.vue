<template>
    <div class="header-container">
        <div class="header-cont-1">
            <div class="header-cont-2">
               <a href="#">our world</a>
            </div>
            <div>
                <div 
                    class="hidden lg:block" 
                    :class="{ 'is-active' : showMenu }"
                >
                    <ul class="ul-cont">
                        <a 
                        href="#"
                        v-for="nav in navEl" 
                        :key="nav.id" 
                        class="li-a-link"
                        >
                            {{ nav.navName }}
                        </a>
                    </ul>
                </div>
            </div>
            <div 
                @click="toggleMenu" 
                class="block lg:hidden text-4xl"
            >
                <span 
                    v-if="showMenu"
                >
                    <i 
                        class='
                            bx bx-x 
                            bg-white 
                            rounded-full 
                            text-orange-500 
                            p-1 
                            font-bold
                        '
                    ></i>
                </span>
                <span 
                    v-else
                >
                    <i 
                        class='
                            bx bx-menu 
                            bg-white 
                            rounded-full 
                            text-orange-500 
                            p-1 
                            font-bold
                        '
                    ></i>
                </span>
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