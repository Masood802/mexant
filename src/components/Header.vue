<script setup>
import { RouterLink, useRouter } from "vue-router";
let router = useRouter();
</script>

<template>
  <div class="w-full h-24 bg-transparent flex justify-between items-center">
    <div class="w-[25%] flex justify-start items-center">
      <img src="logo.png" alt="" class="w-40 ml-5" />
    </div>
    <div class="w-3/6 flex justify-between mr-20 items-center">
      <router-link to="/" class="text-slate-50">Home</router-link>
      <router-link to="/services" class="text-slate-50">Services</router-link>
      <router-link to="/about" class="text-slate-50">about us</router-link>
      <router-link to="contact-us" class="text-slate-50">Contact us</router-link>
      <router-link to="/testimonials" class="text-slate-50">Testimonials</router-link>
      <button class="text-slate-50 bg-green-800 px-4 py-2 rounded" @click="router.push('/contact-us')"> Contact Support</button>
    </div>
  </div>
</template>
