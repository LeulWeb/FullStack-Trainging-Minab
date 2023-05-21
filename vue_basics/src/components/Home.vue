<script setup>
import { ref, reactive } from 'vue';
const isDark = ref(true);

const toggleDark = () => {
    isDark.value = !isDark.value;
}
    //implmeting  night mode
</script>



<template>
    <div :class="{ 'bg-black text-white' :  isDark}" class="container w-[100vw] flex flex-col  h-[100vh]">


        <!--Navigation bars -->
        <div class="container w-11/12 mx-auto my-4">
            <div class="flex justify-between my-2 items-center">
                <div class="w-[10vw]">
                    <img class="w-full" src="../assets/google.png" alt="">
                </div>

                <div>
                    <input value="Bahir Dar" class="border text-black border-blue-500 rounded-full w-[40vw] py-1 px-3"
                        type="text">
                </div>

                <ul class="flex space-x-6 items-center">
                    <li>Gmail</li>
                    <li>Images</li>
                    <li> <i class="fa-solid fa-bars"></i> </li>
                    <li class="bg-blue-500 py-1 px-2 text-white rounded-md">Login</li>
                </ul>
            </div>
        </div>

        <!-- Search Bar -->
        <div class="container w-11/12 mx-auto flex justify-start  border-b-2">
            <ul class="flex space-x-6">
                <li> <i class="fa-solid fa-magnifying-glass"></i> <a href="#">All</a> </li>
                <li> <i class="fa-regular fa-newspaper"></i> <a href="#">News</a> </li>
                <li> <i class="fa-regular fa-image"></i> <a href="#">Images</a> </li>
                <li> <i class="fa-solid fa-video"></i><a href="#"> Videos</a> </li>
                <li> <i class="fa-solid fa-map"></i> <a href="#"> Maps</a> </li>
                <li> <i class="fa-solid fa-ellipsis-vertical"></i><a href="#"> More</a> </li>
                <div @click="toggleDark">
                    <li v-show="isDark"> <i class="fa-regular fa-sun"></i><a href="#">Day</a> </li>
                    <li v-show="!isDark"> <i class="fa-solid fa-moon"></i><a href="#">Night</a> </li>

                </div>
            </ul>
        </div>

        <div class="grid gap-x-10 grid-cols-12 mx-auto w-11/12 mt-2">
            <div class="col-span-8">
                <p class="text-green-500 font-light">Search result for "Bahir Dar"</p>
                <p class="text-blue-500 text-2xl font-medium my-2">Bahir Dar - Wikipedia</p>
                <p class="p-1">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe quaerat autem molestiae neque repellendus
                    perferendis magnam soluta, nulla aperiam dolorum accusamus tenetur facilis aliquid optio, architecto
                    voluptatibus! Deserunt, ipsam totam? Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
                    consectetur neque eum vitae, eos molestiae veritatis illum assumenda harum enim officia soluta autem
                    vel? Aliquid impedit dolorum officia explicabo soluta!
                </p>
                <p class="text-lg font-medium my-2">
                    Pages Suggested for you
                </p>
                <p class="my-1 text-lg">
                    Lake tana
                </p>
                <p class="my-1 text-lg">
                    Lake tana
                </p>
                <p class="my-1 text-lg">
                    Lake tana
                </p>
                <p class="font-medium text-lg">Image results for you</p>
                <div class="grid grid-cols-4 gap-x-3">
                    <img src="../assets/tana.jpg" alt="">
                    <img src="../assets/tana.jpg" alt="">
                    <img src="../assets/tana.jpg" alt="">
                    <img src="../assets/tana.jpg" alt="">
                </div>
            </div>
            <div class="col-span-4  mt-6">
                <div class="flex space-x-3">
                    <div>
                        <img src="../assets/tana.jpg" alt="">
                    </div>
                    <div>
                        <img src="../assets/tana.jpg" alt="">
                    </div>
                </div>

                <div>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem minima nihil distinctio
                        expedita dolor excepturi fuga, eligendi debitis obcaecati. Quisquam eveniet iste suscipit vero
                        placeat ex minima qui accusantium quaerat.lore Lorem, ipsum dolor sit amet consectetur adipisicing
                        elit.
                    </p>
                    <p class="my-2">
                        <strong>This is bold</strong> this is light
                    </p>
                    <p class="my-2">
                        <strong>This is bold</strong> this is light
                    </p>
                    <p class="my-2">
                        <strong>This is bold</strong> this is light
                    </p>
                    <p class="my-2">
                        <strong>This is bold</strong> this is light
                    </p>
                    <p class="my-2 text-lg font-bold">
                        Plan a trip
                    </p>

                    <div class="flex border-b-2 justify-start space-x-3 items-center">
                        <i class="fa-regular fa-image"></i> <span>see images</span>
                    </div>



                </div>
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
  