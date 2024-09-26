<script setup>
import logo from '@/assets/img/logo.jpg'
</script>

<template>
    <nav class="bg-gray-800 text-white py-4 md:py-4 lg:py-4">
      <div class="container mx-auto flex justify-between items-center md:flex-row lg:flex-row flex-col ">

        <div class="flex items-center">
        <img :src="logo" alt="Logo" class="w-20 h-20 rounded-full object-cover">
        <div class=" text-3xl font-bold ml-5">
                logo
        </div>
    </div>
        <ul class="flex items-center space-x-20 ">
            <li><a href="#" class="hover:bg-gray-700 py-4 px-4 rounded-full">Home</a></li>
            <li><a href="#" class="hover:bg-gray-700 py-4 px-4 rounded-full">Categories</a></li>
            <li><a href="#" class="hover:bg-gray-700 py-4 px-4 rounded-full" >Login</a></li>
           
        </ul>
           <input type="text" placeholder="search" class="px-2 py-2 rounded-full outline-none text-black">
      </div>
    </nav>
</template>