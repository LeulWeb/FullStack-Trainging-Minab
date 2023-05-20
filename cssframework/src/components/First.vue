

<template>
  <div class="container w-screen flex flex-col justify-between h-screen ">
    

    <!--Navigation bars -->
    <div class="container w-11/12 mx-auto">
      
    <div class="flex justify-end my-2 items-center">
      <ul class="flex space-x-6 items-center">
        <li>Gmail</li>
        <li>Images</li>
        <li> <i class="fa-solid fa-bars"></i> </li>
        <li class="bg-blue-500 py-1 px-2 text-white rounded-md">Login</li>
      </ul>
    </div>

    <!-- Search Bar -->
    <div class="w-full flex h-[60vh] justify-center items-center flex-col">
      <div class="w-[25vw]">
        <img class="w-full" src="../assets/google.png" alt="">
      </div>
      <div>
        <input placeholder="Search" class="w-[40vw] my-4 border border-blue-500 rounded-full py-1 px-3" type="text" name="" id="">
      </div>

      <div class="flex space-x-3">
        <button class="bg-gray-300 shadow-lg p-2">
          Google Search
        </button>
        <button class="bg-gray-300 shadow-lg p-2">
          I am feeling Lucky
        </button>
      </div>
      
      <div class="flex space-x-3 mt-4">
        <p>Google is avialbe in:- </p>
        <span class="text-blue-500 font-medium">Amharic</span>
        <span class="text-blue-500 font-medium">English</span>
        <span class="text-blue-500 font-medium">Tigrigna</span>
        <span class="text-blue-500 font-medium">Afam Ormo</span>
      </div>

    </div>
    </div>


    <!-- Footer -->

    <div class="bg-gray-200 w-screen ">
      <div class="border border-gray-500 p-1">
        <p>Ethiopia</p>
      </div>
      <div>
        <ul class="flex space-x-6 items-center p-1">
          <li>Advertising</li>
          <li>Business</li>
          <li>How Search Works</li>
        </ul>
      </div>
    </div>
  </div>



  

</template>

<!-- <style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style> -->
