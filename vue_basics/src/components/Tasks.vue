<script setup>
import { ref, reactive } from "vue";

const isDark = ref(false);

const toggleDark = () => {
  isDark.value = !isDark.value;
};

let products = ref([
  {
    id: 1,
    src: "src/assets/ma.jpg",
    title: "Macbook Pro",
    description:
      "This is some cool product which is invinted and do not read this text it is just descrption and dummy text not legin please do not waste your time on reading this",
    price: 2000,
    inventory: 5,
  },
  {
    id: 2,
    src: "src/assets/ma.jpg",
    title: "Macbook Air",
    description:
      "This is some cool product which is invinted and do not read this text it is just descrption and dummy text not legin please do not waste your time on reading this",
    price: 1500,
    inventory: 10,
  },
  {
    id: 3,
    src: "src/assets/ma.jpg",
    title: "iMac",
    description:
      "This is some cool product which is invinted and do not read this text it is just descrption and dummy text not legin please do not waste your time on reading this",
    price: 2500,
    inventory: 2,
  },
  {
    id: 4,
    src: "src/assets/ma.jpg",
    title: "iMac Pro",
    price: 5000,
    inventory: 0,
    description:
      "This is some cool product which is invinted and do not read this text it is just descrption and dummy text not legin please do not waste your time on reading this",
  },
]);

const removeProduct = (id) => {

 
    let newProduct = products.value.filter((product) => product.id !== id);
    products.value = newProduct;
  console.log(products.value);
  // products.splice(id, 1);
};
</script>

<template>
  <div
    class="w-screen h-screen overflow-x-hidden"
    :class="{ 'bg-black text-white': isDark }"
  >
    <div class="w-screen h-screen" id="hero">
      <iframe
        src="https://my.spline.design/macbookprocopy-50c6c534783f7cda828784827bacbc57/"
        frameborder="0"
        width="100%"
        height="100%"
      ></iframe>
    </div>
    <div :class="{ 'bg-black text-white': isDark }">
      <div
        class="w-8/12 mx-auto my-3 flex justify-between"
        :class="{ 'bg-black text-white': isDark }"
      >
        <p class="font-bold text-3xl">Order Us Now</p>
        <button @click="toggleDark">
          <div v-show="isDark"><i class="fa-regular fa-sun"></i> Day</div>
          <div v-show="!isDark"><i class="fa-regular fa-moon"></i> Night</div>
        </button>
      </div>

      <div
        class="w-8/12 mx-auto grid gap-5 grid-cols-2 my-3"
        :class="{ 'bg-black text-white': isDark }"
      >

      <div v-if="products.length == 0">
         No Products
      </div>
        <div 
          v-for="item in products"
          class="shadow-md rounded-lg hover:animate-pulse"
        >
          <img v-bind:src="item.src" alt="" />
          <div class="p-2">
            <p class="">{{ item.title }}</p>
            <p class="font-light">
              {{ item.description }}
            </p>
            <p class="font-medium text-2xl">{{ item.price }} Birr</p>
            <div class="flex justify-between">
              <p class="font-medium text-lg">{{ item.inventory }} left</p>
              <button @click="removeProduct(item.id)">
                <i class="fa-solid fa-trash"></i>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#hero {
  background-image: url(https://my.spline.design/macbookprocopy-50c6c534783f7cda828784827bacbc57/);
}
</style>
