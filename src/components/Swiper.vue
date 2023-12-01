<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import {
  Navigation,
  Pagination,
  Scrollbar,
  A11y,
  Autoplay,
} from "swiper/modules";
import Header from "../components/Header.vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";
import { ref } from "vue";
import { useRouter } from "vue-router";
let router = useRouter();
let slides = ref([
  {
    id: 1,
    title: "Get ready for your business  & upgrade",
    last: "all aspects",
    detail:
      "Mexant HTML5 Template is provided for free of charge. This layout is based on Boostrap 5 CSS framework. Anyone can download and edit for any professional website. Thank you for visiting TemplateMo website.",
    image: "slide-01.jpg",
  },
  {
    id: 2,
    title: "Digital Currency for you & Best ",
    last: "Crypto Tips",
    detail:
      "You will see a bunch of free CSS templates when you search on Google. TemplateMo website is probably the best one because it is 100% free. It does not ask you anything in return. You have a total freedom to use any template for any purpose.",
    image: "slide-02.jpg",
  },
  {
    id: 3,
    title: "Best One in Town & ",
    last: "Crypto Services",
    detail:
      "When you browse through different tags on TemplateMo website, you can see a variety of CSS templates which are responsive website designs for different individual needs. Please tell your friends about our website. Thank you",
    image: "slide-03.jpg",
  },
]);
</script>

<template>
  <div class="w-full absolute z-50 top-0">
    <Header></Header>
  </div>
  <swiper
    class="w-full h-screen"
    :loop="true"
    :pagination="{ clickable: true }"
    :modules="[Navigation, Pagination, Scrollbar, A11y, Autoplay]"
    navigation
    :scrollbar="{ draggable: true }"
    :autoplay="{
      delay: 3000,
      disableOnInteraction: false,
      pauseOnMouseEnter: true,
    }"
  >
    <swiper-slide v-for="slide in slides" :key="slide.id">
      <div class="relative w-full">
        <div class="w-3/5 text-7xl font-bold text-slate-50 ml-20 absolute">
          <h1 class="mt-20 mb-4">{{ slide.title }}</h1>
          <h1 class="text-orange-700">{{ slide.last }}</h1>
          <p class="text-base my-16 w-[70%] font-semibold">
            {{ slide.detail }}
          </p>
        </div>
        <div><img :src="slide.image" /></div>
      </div>
      <div class="absolute left-20 bottom-20 flex">
        <button
          @click="router.push('/services')"
          class="w-30 bg-green-600 mx-6 px-12 py-2 my-6 rounded flex justify-center items-center text-slate-50 text-center"
        >
          Discover More
        </button>
        <button
          @click="router.push('contact-us')"
          class="w-30 bg-orange-600 mx-6 px-16 py-2 my-6 rounded text-slate-50 text-center flex justify-center items-center"
        >
          Contact Us
        </button>
      </div>
    </swiper-slide>
  </swiper>
</template>
