<script setup>
import { ref} from 'vue';

const showImage = ref(false);

function toggleImage() {
    showImage.value = !showImage.value;
}

</script>

<template>
    <nav>
        <ul  class="flex justify-end space-x-3 my-4">
            <li>Gmail</li>
            <li>Images</li>
            <li><i class="fa-solid fa-grid"></i></li>
            <li>
                <button @click="toggleImage" class="bg-blue-500 py-1 px-2 text-white rounded-md">sign in</button>
            </li>
        </ul>
    </nav>



      <div class="w-full flex h-[60vh] justify-center items-center flex-col">
          <div class="w-[25vw]">
            <img v-show="showImage" class="w-full" src="../assets/google.png" alt="">
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
</template>


<style scoped> 
</style>