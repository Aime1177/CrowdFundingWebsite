

<template>
    <nav class="bg-gray-900 text-white py-10  
    sticky top-0 z-10 transition-shadow duration-300" :class="{'shadow-lg': isScrolled}
    ">
      <div class="container mx-auto flex justify-between items-center md:flex-row lg:flex-row flex-col ">

        <div class="flex items-center">
        
        <div class=" text-3xl font-bold ml-5 animate-bounce">
                CROWD <br><span class="text-red-600 text-5xl">
                FUNDING</span>
        </div>
    </div>
        <ul class="flex items-center space-x-20 text-xl">
            <li><a href="#" class="nav-link hover:bg-gray-700 py-4 px-4 rounded-full">Home</a></li>
            <li><a href="#" class="nav-link hover:bg-gray-700 py-4 px-4 rounded-full">Categories</a></li>
            <li><a href="#" class="nav-link hover:bg-gray-700 py-4 px-4 rounded-full" >Login</a></li>
          
           
        </ul>
        <input type="search" class="py-2 pl-10 text-gray-900 pr-4 rounded-lg shadow-md focus:shadow-lg focus:outline-none focus:ring focus:ring-indigo-500" placeholder="Search">

      </div>
      
      
    </nav>
</template>
<style scoped>
.nav-link {
  color: white;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #fbbf24; 
}
</style>