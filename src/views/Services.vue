<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
</script>

<template>
  <div class="bg-gray-900 fixed w-full top-0">
    <Header></Header>
  </div>
  <div class="w-[80%] mt-32 mx-auto flex justify-between items-center">
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 mr-10 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-archive"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">CSS Templates</h1>
        <p class="font-semibold">
          TemplateMo website is the best for you to explore and download free
          website templates.
        </p>
      </div>
    </div>
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-cloud"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">HTML5 Web Pages</h1>
        <p class="font-semibold">
          Templates are based on Bootstrap 5 CSS framework. You can easily adapt
          or modify based on your needs.
        </p>
      </div>
    </div>
  </div>
  <div class="w-[80%] my-10 mx-auto flex justify-between items-center">
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 mr-10 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-charging-station"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">Responsive Designs</h1>
        <p class="font-semibold">
          All of our CSS templates are 100% free to use for commercial or
          business websites.
        </p>
      </div>
    </div>
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-suitcase"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">Mobile and Tablet ready!</h1>
        <p class="font-semibold">
          Our HTML CSS templates are well-tested on mobile, tablet, and desktop
          compatibility.
        </p>
      </div>
    </div>
  </div>
  <div class="w-[80%] my-10 mx-auto flex justify-between items-center">
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 mr-10 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-archway"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">Fast Customer Support</h1>
        <p class="font-semibold">
          Do not be hesitated to contact us if you have any question or concern
          about our templates.
        </p>
      </div>
    </div>
    <div
      class="w-[50%] shadow-lg border border-slate-100 py-16 px-4 flex items-center justify-center rounded"
    >
      <div
        class="text-6xl px-6 text-green-700 mt-0 hover:mt-4 transition-all ease-linear duration-300"
      >
        <i class="fas fa-puzzle-piece"></i>
      </div>
      <div class="w-full">
        <h1 class="text-2xl font-bold">Fully Customizable</h1>
        <p class="font-semibold">
          If you have any idea or suggestion about new templates, feel free to
          let us know.
        </p>
      </div>
    </div>
  </div>
  <Footer></Footer>
</template>
