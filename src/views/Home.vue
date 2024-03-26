<template>
    <div>
        <Section1 />
        <section2 />
        <Section3 />
        <Section4 
            v-slot="nameItems"
        >
            <a href="#">
                <div 
                    class="section4-home-1"
                >
                    <div>
                        <img 
                            :src="nameItems.itemImg" 
                            class="section4-home-img" 
                            alt=""
                        >
                    </div>
                    <div 
                        class="p-4 text-center"
                    >
                        <div 
                            class="section4-home-title-name"
                        >
                            {{ nameItems.itemName }}
                        </div>
                        <div>
                            {{ nameItems.itemText }} 
                        </div>
                    </div>
                </div>
            </a>
        </Section4>
        <NewsLetter />
    </div>
</template>

<script setup>
    import Section1 from '@/views/astrofirstpage/Section1.vue';
    import Section2 from '@/views/astrofirstpage/Section2.vue';
    import Section3 from '@/views/astrofirstpage/Section3.vue';
    import Section4 from '@/views/astrofirstpage/Section4.vue';
    import NewsLetter from '@/views/astrofirstpage/NewsLetter.vue';
</script>
