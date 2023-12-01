<script setup>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import $ from "jquery";
import { onMounted } from "vue";
import { useRouter } from "vue-router";
let router = useRouter();
onMounted(() => {
  window.addEventListener("scroll", () => {
    if (window.scrollY < 300) {
      document.getElementById("header").style.backgroundColor = "transparent";
    } else {
      document.getElementById("header").style.backgroundColor = "black";
    }
  });
});

function hide() {
  $("#up").show();
  $("#down").hide();
  $("#para").hide();
}
function show() {
  $("#up").hide();
  $("#down").show();
  $("#para").show();
}
</script>

<template>
  <div class="bg-gray-900 bg-[url('heading-bg.jpg')] bg-cover w-full h-96">
    <Header class="fixed top-0" id="header"></Header>
    <div
      class="text-6xl font-bold text-slate-100 border-b-4 mx-auto text-center w-[20%] pt-24 pb-6"
    >
      About Us
    </div>
  </div>
  <div class="w-[80%] h-screen mx-auto my-20 flex justify-between items-center">
    <div class="w-1/2 mx-10 my-auto">
      <img src="about-left-image.jpg" />
    </div>
    <div class="w-1/2 rounded-lg shadow-lg h-[550px] border-b-1">
      <div>
        <h1 class="text-2xl font-bold text-green-700 py-2 ml-4 my-4">
          Mexant Financial Planning
          <i
            class="fas fa-chevron-right ml-16 hidden"
            id="up"
            @click="show"
          ></i>
          <i class="fas fa-chevron-down ml-16" id="down" @click="hide"></i>
        </h1>
        <p class="text-base mx-6 my-3" id="para">
          You will see a bunch of free CSS templates when you search on Google.
          TemplateMo website is probably the best one because it is 100% free.
          We do not ask you anything in return. You are free to use our
          templates for any purpose.
        </p>
        <hr class="w-[90%] mx-auto" />
      </div>

      <div>
        <h1 class="text-2xl font-bold text-green-700 py-2 ml-4 my-3">
          Mexant Crypto Investing
          <i
            class="fas fa-chevron-right ml-16 hidden"
            id="up"
            @click="show"
          ></i>
          <i class="fas fa-chevron-down ml-16" id="down" @click="hide"></i>
        </h1>
        <p class="text-base mx-6 my-3" id="para">
          Mexant HTML5 Template is available to download 100% free of charge.
          This CSS layout is based on Boostrap 5 framework. Anyone can edit and
          use this layout for all professional websites. Thank you for visiting
          TemplateMo website.
        </p>
        <hr class="w-[90%] mx-auto" />
      </div>

      <div>
        <h1 class="text-2xl font-bold text-green-700 py-2 ml-4 my-3">
          Cryptocurrency Investments
          <i
            class="fas fa-chevron-right ml-16 hidden"
            id="up"
            @click="show"
          ></i>
          <i class="fas fa-chevron-down ml-16" id="down" @click="hide"></i>
        </h1>
        <p class="text-base mx-6 my-3" id="para">
          Ut dictum vehicula massa, ac pharetra leo tincidunt eu. Phasellus in
          tristique magna, ac gravida leo. Integer sed lorem sapien. Ut viverra
          mauris sed lobortis commodo. Mauris scelerisque venenatis justo, sed
          interdum sem.
        </p>
        <hr class="w-[90%] mx-auto" />
      </div>
    </div>
  </div>
  <div
    class="w-full bg-[url('cta-bg.jpg')] bg-cover h-[250px] flex justify-between items-center px-24"
  >
    <div>
      <h1 class="text-4xl font-bold text-slate-50">
        Business <span class="text-green-600">Solutions</span> and <br /><span
          class="text-orange-700"
          >Crypto </span
        >Investments
      </h1>
    </div>
    <div class="flex">
      <button
        @click="router.push('/services')"
        class="w-30 bg-green-600 mx-6 px-6 py-2 my-6 rounded flex justify-center items-center text-slate-50 text-center text-sm"
      >
        Discover More
      </button>
      <button
        @click="router.push('contact-us')"
        class="w-30 bg-orange-600 mx-6 px-10 py-2 my-6 rounded text-slate-50 text-center flex justify-center items-center text-sm"
      >
        Contact Us
      </button>
    </div>
  </div>
  <div class="w-4/5 mx-auto flex justify-between items-center">
    <div class="w-[50%] flex justify-center flex-col items-center my-20">
      <h1 class="text-2xl font-bold mx-10">
        Please tell us about your idea and how you want it to be
      </h1>
      <p class="mx-10 my-6 text-left">
        If you need more HTML templates, you can try visiting Too CSS blog and
        Tooplate websites. You can get many good templates on those websites.<br /><br />
        Nulla non placerat neque, a gravida elit. Vestibulum ante ipsum primis
        in faucibus orci luctus et ultrices posuere cubilia curae; Morbi sed
        dolor condimentum tellus commodo volutpat non malesuada turpis.
      </p>
      <button
        class="w-30 bg-green-600 mx-auto px-6 py-2 my-6 rounded flex justify-center items-center text-slate-50 text-center text-sm"
      >
        Discover More
      </button>
    </div>
    <div class="w-[50%] flex justify-between items-center flex-wrap">
      <div
        class="w-[250px] h-[200px] shadow-lg flex justify-center items-center flex-col relative my-5"
      >
        <h1 class="text-xl font-bold px-6 mb-4">First Step</h1>
        <span
          class="absolute top-2 text-green-700 text-4xl font-bold right-3 hover:top-4 transition-all duration-700"
          >01</span
        >
        <p class="px-1 text-center">
          Pellentesque ipsum elit,<br />
          congue a sapien laoreet, pellentesque ultricies risus.
        </p>
      </div>
      <div
        class="w-[250px] h-[200px] shadow-lg flex justify-center items-center flex-col relative"
      >
        <h1 class="text-xl font-bold px-6 mb-4">Second Step</h1>
        <span
          class="absolute top-2 text-green-700 text-4xl font-bold right-3 hover:top-4 transition-all duration-700"
          >02</span
        >
        <p class="px-1 text-center">
          Pellentesque ipsum elit,<br />
          congue a sapien laoreet, pellentesque ultricies risus.
        </p>
      </div>
      <div
        class="w-[250px] h-[200px] shadow-lg flex justify-center items-center flex-col relative"
      >
        <h1 class="text-xl font-bold px-6 mb-4">Thirdt Step</h1>
        <span
          class="absolute top-2 text-green-700 text-4xl font-bold right-3 hover:top-4 transition-all duration-700"
          >03</span
        >
        <p class="px-1 text-center">
          Pellentesque ipsum elit,<br />
          congue a sapien laoreet, pellentesque ultricies risus.
        </p>
      </div>
      <div
        class="w-[250px] h-[200px] shadow-xl flex justify-center items-center flex-col relative border rounded-lg border-slate-100"
      >
        <h1 class="text-xl font-bold px-6 mb-4">Fourth Step</h1>
        <span
          class="absolute top-2 text-green-700 text-4xl font-bold right-3 hover:top-4 transition-all duration-700"
          >04</span
        >
        <p class="px-1 text-center">
          Pellentesque ipsum elit,<br />
          congue a sapien laoreet, pellentesque ultricies risus.
        </p>
      </div>
    </div>
  </div>
  <Footer></Footer>
</template>
