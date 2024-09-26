<script setup>
 import { ref } from 'vue';
 import  panel from '@/assets/img/img/panel.jpeg'
 import animal from '@/assets/img/img/animal.jpeg'
 import artist from '@/assets/img/img/artist.webp'
 import supplies from '@/assets/img/img/supplies.webp'
 
 
 const Campaigns = ref([
    {
        title:"Panels for school",
        img:panel,
        goal:"Goal:$50,000",
        raised:"Raised:$35,000",
        donors:"Donors:110",
        progress:200 
    },
    {
        title:"Help build Animal Shelter",
        img:animal,
        goal:"Goal:$30,000",
        raised:"Raised:$22,000",
        donors:"Donors:150",
        progress:250 
    },
    {
        title:"Support Local Artist",
        img:artist,
        goal:"Goal:$26,000",
        raised:"Raised:$18,000",
        donors:"Donors:45",
        progress: 150
    },
    {
        title:"Medical supplies for hospitals",
        img:supplies,
        goal:"Goal:$10,000",
        raised:"Raised:$6,000",
        donors:"Donors:85",
        progress: 200 
    },
    
 ])

</script>

<template>
    <section class="flex justify-between gap-8  text-center mx-10 mb-48">
    
    <div v-for="(Campaign , index ) in Campaigns" :key="index"
     class="w-1/4 bg-white border rounded-lg shadow-md p-4 flex
      flex-col justify-between mt-10  mb-10 transition duration-300 ease-out hover:scale-110 cursor-pointer ">

    
        <img :src="Campaign.img" alt="image" class="w-full h-48 object-cover mb-4 rounded-lg" />
        
        <h3 class="text-xl font-bold">{{ Campaign.title }}</h3>
        <p>{{ Campaign.goal }}</p>
        <p>{{ Campaign.raised }}</p>
        <p>{{ Campaign.donors }}</p>
    
        
       
        <div class="w-full bg-gray-200 rounded-full h-2 mb-4 ml-4" style="width: 300px;">
            <div class="bg-green-400 h-2 rounded-full" :style="{width: Campaign.progress + 'px'}"></div>
        </div>
        
        <button class="w-[300px] transition duration-300 ease-out hover:scale-110 cursor-pointer bg-blue-500 text-white py-2 mb-4 ml-4 rounded">View Campaign</button>
    </div>
    


</section>


    
</template>