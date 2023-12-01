<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import { onMounted } from "vue";
onMounted(() => {
  window.addEventListener("scroll", () => {
    if (window.scrollY < 300) {
      document.getElementById("header").style.backgroundColor = "transparent";
    } else {
      document.getElementById("header").style.backgroundColor = "black";
    }
  });
});
</script>

<template>
  <div class="bg-gray-900 bg-[url('heading-bg.jpg')] bg-cover w-full h-96">
    <Header class="fixed top-0 z-50" id="header"></Header>
    <div
      class="text-6xl font-bold text-slate-100 border-b-4 mx-auto text-center w-[25%] pt-52 pb-6"
    >
      Contact Us
    </div>
  </div>
  <div class="w-[80%] mx-auto mt-32 relative">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d13987.542336008242!2d70.37942689134829!3d28.782672216090635!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3930aa29f5de2651%3A0x69e575de73d5d25f!2sRukanpur%2C%20Rahim%20Yar%20Khan%2C%20Punjab%2C%20Pakistan!5e0!3m2!1sen!2s!4v1701161348544!5m2!1sen!2s"
      class="w-full h-[500px] my-10"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
    ></iframe>
    <div
      class="w-[300px] h-[200px] rounded-lg shadow-xl flex justify-center items-center flex-col absolute top-[450px] z-40 bg-white left-16 hover:top-[430px] transition-all duration-700"
    >
      <i class="fas fa-envelope text-green-600 text-4xl my-2"></i>
      <h1 class="text-2xl font-bold">Email Address</h1>
      <h2 class="text-lg font-bold text-green-700 hover:text-orange-700">masoodsse@gmail.com</h2>
    </div>
    <div
      class="w-[300px] h-[200px] rounded-lg shadow-xl flex justify-center items-center flex-col absolute top-[450px] z-40 bg-white left-72 mx-28 hover:top-[430px] transition-all duration-700"
    >
      <i class="fas fa-phone-alt text-green-600 text-4xl my-2"></i>
      <h1 class="text-2xl font-bold">Phone Number</h1>
      <h2 class="text-lg font-bold text-green-700 hover:text-orange-700">+923003370270</h2>
    </div>
    <div
      class="w-[300px] h-[200px] rounded-lg shadow-xl flex justify-center items-center flex-col absolute top-[450px] z-40 bg-white left-96 mx-[350px] hover:top-[430px] transition-all duration-700"
    >
      <i class="fas fa-map-marked-alt text-green-600 text-4xl my-2"></i>
      <h1 class="text-2xl font-bold">Address</h1>
      <h2 class="text-lg font-bold text-green-700 hover:text-orange-700">GHS Rukan Pur</h2>
    </div>
  </div>
  <div class="w-4/5 mx-auto my-52">
    <h2 class="text-2xl text-center font-bold my-6 text-orange-700">
      Contact Us
    </h2>
    <h1 class="text-4xl text-center font-bold mb-4">Feel free to message us</h1>
    <div class="w-4/5 mx-auto mt-20 my-4">
      <input
        type="text"
        name="name"
        placeholder="Your Name..."
        class="w-[45%] mx-2 bg-gray-200 px-3 py-2 rounded outline-none"
      />
      <input
        type="text"
        name="phone"
        placeholder="Your Phone..."
        class="w-[45%] mx-2 bg-gray-200 px-3 py-2 rounded outline-none"
      />
    </div>
    <div class="w-4/5 mx-auto my-4">
      <input
        type="text"
        name="name"
        placeholder="Your E-mail..."
        class="w-[45%] mx-2 bg-gray-200 px-3 py-2 rounded outline-none"
      />
      <input
        type="text"
        name="phone"
        placeholder="Subject"
        class="w-[45%] mx-2 bg-gray-200 px-3 py-2 rounded outline-none"
      />
    </div>
    <div class="w-4/5 mx-auto my-4">
      <textarea
        name=""
        id="sms"
        placeholder="Your Massage"
        class="w-[92%] mx-2 bg-gray-200 h-36 px-2 py-3 rounded outline-none"
      ></textarea>
    </div>
    <button
      class="w-52 bg-orange-600 mx-28 px-10 py-3 my-1 rounded text-slate-50 text-center flex justify-center items-center"
    >
      Send Massage
    </button>
  </div>
  <Footer></Footer>
</template>
