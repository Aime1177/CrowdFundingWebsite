<template>
    <footer class="bg-gray-900 text-white py-12">
      <div class="container mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
       
        <div>
          <h3 class="text-2xl font-bold mb-4">About Us</h3>
          <p class="text-gray-400">
            We are dedicated to bringing communities together to support meaningful causes through crowdfunding. Join us in making a difference!
          </p>
          <div class="mt-4">
            <h4 class="font-semibold">Connect with us:</h4>
            <div class=" ">
              <a href="#" class="hover:text-gray-300">
                <i class="fab fa-facebook-f"></i> 
              </a>
              <a href="#" class="hover:text-gray-300">
                <i class="fab fa-twitter"></i>
              </a>
              <a href="#" class="hover:text-gray-300">
                <i class="fab fa-linkedin-in"></i>
              </a>
              <a href="#" class="hover:text-gray-300">
                <i class="fab fa-instagram"></i>
              </a>
            </div>
          </div>
        </div>
  
       
        <div>
          <h3 class="text-2xl font-bold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li>
              <a href="#" class="hover:underline hover:text-gray-300">Home</a>
            </li>
            <li>
              <a href="#" class="hover:underline hover:text-gray-300">Projects</a>
            </li>
            <li>
              <a href="#" class="hover:underline hover:text-gray-300">About</a>
            </li>
            <li>
              <a href="#" class="hover:underline hover:text-gray-300">Contact Us</a>
            </li>
          </ul>
        </div>
  
        
        <div>
          <h3 class="text-2xl font-bold mb-4">Newsletter</h3>
          <p class="text-gray-400 mb-4">
            Subscribe to get the latest updates on new projects and exclusive offers.
          </p>
          <form class="flex items-center space-x-2">
            <input
              type="email"
              class="w-full px-4 py-2 text-gray-800 rounded-lg focus:outline-none focus:ring-2 focus:ring-pink-500"
              placeholder="Enter your email"
              required
            />
            <button class="px-6 py-2 bg-gradient-to-r from-purple-500 via-pink-500 to-red-500 text-white font-semibold rounded-lg shadow-md hover:shadow-xl transition duration-300 ease-in-out">
              Subscribe
            </button>
          </form>
        </div>
      </div>
  
      <div class="mt-12 border-t border-gray-700 pt-8 text-center text-gray-500">
        <p>&copy; 2024 Crowdfunding Inc. All rights reserved.</p>
      </div>
    </footer>
  </template>