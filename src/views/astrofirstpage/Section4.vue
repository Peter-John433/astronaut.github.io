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

  const items = ref([
    {
        title : 'astronaut',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : 'src/assets/img/astronaut-1.png',
        id : 1
    },
    {
        title : 'outer space',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : 'src/assets/img/outer-space.png',
        id : 2
    },
    {
        title : 'stars',
        text : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facilis exercitationem facere, inventore quidem vero eaque nam, quibusdam aperiam ducimus quasi obcaecati omnis blanditiis in dolor? Cumque voluptatibus quibusdam aliquid velit.',
        img : 'src/assets/img/stars.png',
        id : 3
    }
  ])
</script>
