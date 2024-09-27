<template>
    <div class="min-h-screen bg-gradient-to-r from-purple-400 via-pink-500 to-red-500 flex justify-center items-center">
      <div class="bg-white rounded-lg shadow-xl p-10 w-full max-w-lg transition-all duration-500 transform hover:scale-105">
        <h2 class="text-4xl font-bold text-center text-gray-800 mb-8">
          Welcome 
        </h2>
        <form class="space-y-6">
          
          <div>
            <input 
              type="email" 
              id="email" 
              class="block w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm text-gray-700 placeholder-gray-500 focus:ring-4 focus:ring-purple-300 focus:border-purple-500 transition duration-300 ease-in-out" 
              placeholder="Enter your email" 
              required 
            />
          </div>
  
          
          <div class="relative">
            <input 
              type="password" 
              id="password" 
              class="block w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm text-gray-700 placeholder-gray-500 focus:ring-4 focus:ring-pink-300 focus:border-pink-500 transition duration-300 ease-in-out peer" 
              placeholder="Enter your password" 
              required 
            />
          </div>
  
         
          <div class="flex items-center justify-between">
            <label class="flex items-center">
              <input type="checkbox" class="form-checkbox text-purple-500 transition duration-300 ease-in-out">
              <span class="ml-2 text-gray-700">Remember me</span>
            </label>
            <a href="#" class="text-sm text-purple-500 hover:text-purple-600 transition duration-300 ease-in-out">Forgot Password?</a>
          </div>
  
          
          <button 
            type="submit" 
            class="w-full py-3 bg-gradient-to-r from-purple-500 via-pink-500 to-red-500 text-white font-semibold rounded-lg shadow-md hover:shadow-xl transition duration-300 ease-in-out transform hover:-translate-y-1 hover:scale-105">
            Sign In
          </button>
  
          
          <div class="flex items-center justify-center space-x-2 text-gray-400">
            <span class="block h-px w-16 bg-gray-300"></span>
            <span>OR</span>
            <span class="block h-px w-16 bg-gray-300"></span>
          </div>
  
          
          <div class="flex space-x-4">
            <button 
              type="button" 
              class="w-full py-3 bg-blue-500 text-white font-semibold rounded-lg shadow-md hover:shadow-xl transition duration-300 ease-in-out transform hover:-translate-y-1 hover:scale-105">
              Sign in with Facebook
            </button>
            <button 
              type="button" 
              class="w-full py-3 bg-gray-800 text-white font-semibold rounded-lg shadow-md hover:shadow-xl transition duration-300 ease-in-out transform hover:-translate-y-1 hover:scale-105">
              Sign in with Google
            </button>
          </div>
        </form>
      </div>
    </div>
  </template>