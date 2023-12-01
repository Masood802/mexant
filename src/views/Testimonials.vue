<script setup>
import Header from "../components/Header.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import {
  Navigation,
  Pagination,
  Scrollbar,
  A11y,
  Autoplay,
} from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
import { ref } from "vue";
let slides = ref([
  {
    id: 1,
    name: "Masood Ur Rehman",
    desig: "CEO of Mexant",
    img: "masood.jpg",
    quote:
      "“Donec et nunc massa. Nullam non felis dignissim, dapibus turpis semper, vulputate lorem. Nam volutpat posuere tellus, in porttitor justo interdum nec. Aenean in dapibus risus, in euismod ligula. Aliquam vel scelerisque elit.”",
  },
  {
    id: 2,
    name: "Andrew Garfield",
    desig: "CTO of Mexant",
    img: "testimonials-01.jpg",
    quote:
      "“Etiam id ligula risus. Fusce fringilla nisl nunc, nec rutrum lectus cursus nec. In blandit nibh dolor, at rutrum leo accumsan porta. Nullam pulvinar eros porttitor risus condimentum tempus.”",
  },
  {
    id: 1,
    name: "George Lopez",
    desig: "Crypto Manager",
    img: "testimonials-01.jpg",
    quote:
      "“Ut dictum vehicula massa, ac pharetra leo tincidunt eu. Phasellus in tristique magna, ac gravida leo. Integer sed lorem sapien. Ut viverra mauris sed lobortis commodo.”",
  },
]);
</script>

<template>
  <div class="bg-gray-900">
    <Header></Header>
  </div>
  <div class="w-2/3 mx-auto text-center mt-10">
    <h2 class="text-2xl font-bold text-orange-700 py-6">Testimonials</h2>

    <h1 class="text-4xl font-bold text-green-700 py-2">What They Say</h1>
  </div>
  <div>
    <swiper
      class="w-2/3 h-80 mt-6"
      :loop="true"
      slides-per-view="1"
      :pagination="{ clickable: true }"
      :modules="[Pagination, A11y, Autoplay]"
      :autoplay="{
        delay: 3000,
        disableOnInteraction: false,
        pauseOnMouseEnter: true,
      }"
    >
      <swiper-slide v-for="slide in slides" :key="slide.id">
        <div
          class="relative w-full h-full flex justify-between bg-slate-50 shadow-lg"
        >
          <div class="w-[60%] relative">
            <i
              class="fas fa-quote-left w-20 h-20 bg-green-700 text-4xl rounded-lg mx-auto text-center text-slate-50 flex items-center justify-center absolute top-4 left-8"
            ></i>
            <p class="text-left mx-6 mt-20 pt-10 font-semibold">
              {{ slide.quote }}
            </p>
            <h1 class="text-xl font-bold text-green-700 mx-6 mt-4">
              {{ slide.name }}
            </h1>
            <h1 class="text-orange-700 px-6 my-2 text-sm font-semibold">
              {{ slide.desig }}
            </h1>
          </div>
          <div class="w-[30%] h-full">
            <img
              :src="slide.img"
              class="overflow-hidden w-full h-full rounded-r-lg"
            />
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
