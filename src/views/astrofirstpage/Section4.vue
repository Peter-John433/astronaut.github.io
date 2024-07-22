<template>
    <div class="section4-I">
        <div class="container section4-II">
            <slot  
                v-for="item in items" 
                :itemName="item.title" 
                :itemText="item.text" 
                :itemImg="item.img" 
                :key="item.id"
            ></slot>
        </div>
    </div>
</template>

<script setup>
  import { ref } from 'vue';
  import image1 from '@/assets/img/astronaut-1.png'
  import image2 from '@/assets/img/outer-space.png'
  import image3 from '@/assets/img/stars.png'


  const items = ref([
    {
        title : 'astronaut',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : image1,
        id : 1
    },
    {
        title : 'outer space',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : image2,
        id : 2
    },
    {
        title : 'stars',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : image3,
        id : 3
    }
  ])
</script>
