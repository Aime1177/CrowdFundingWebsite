
<script setup>
import water from '@/assets/img/img/water.jpeg'
</script>


<template>
    
    <section class="p-6">
     <h2 class="text-3xl font-bold">Campaign Title</h2>
     <img :src="water" alt="Campaign" class="w-64 h-64 object-cover my-4 rounded-lg" />
     <p class="text-lg mb-4">Campaign Description...</p>
     <div class="w-64 bg-gray-200 rounded-full h-2 mb-4">
       <div class="bg-green-500 h-2 rounded-full" style="width: 200px;"></div>
     </div>
     <button class="px-6 py-2 bg-blue-500 text-white rounded">Donate Now</button>
   </section>

</template>