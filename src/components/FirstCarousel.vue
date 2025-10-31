<template>
  <div class="mt-22">
    <h1 class="text-xl text-start">Masculino</h1>

    <div>
      <Swiper
        :modules="[Navigation]"
        :slides-per-view="4"
        :space-between="1"
        :loop="true"
        :navigation="{ nextEl: '.button-next', prevEl: '.button-prev' }"
        :breakpoints="{
          320: { slidesPerView: 1 },
          640: { slidesPerView: 2 },
          1024: { slidesPerView: 4 },
          1440: { slidesPerView: 5 },
        }"
        class="relative"
      >
        <SwiperSlide v-for="(product, index) in kimonos" :key="index">
          <div class="bg-white p-4 mx-auto">
            <!-- Carrossel de imagens do produto -->
            <Swiper
              :modules="[Navigation]"
              :slides-per-view="1"
              :loop="true"
              :navigation="{ nextEl: '.custom-next', prevEl: '.custom-prev' }"
              class="rounded-t-sm relative"
            >
              <SwiperSlide v-for="(image, i) in product.images" :key="i">
                <img
                  :src="image"
                  :alt="product.title"
                  class="w-full h-96 object-cover rounded-t-sm"
                />
              </SwiperSlide>
            </Swiper>

            <!-- Informações do produto -->
            <div class="text-start mt-1">
              <h2 class="font-semibold">{{ product.title }}</h2>

              <h1 class="font-semibold mt-2">R$ {{ product.price }}</h1>
            </div>
          </div>
        </SwiperSlide>

        <button
          class="button-prev absolute z-10 top-1/2 left-1 transform -translate-y-1/2 text-[#366C90] bg-gray-100 shadow-md p-1 rounded-full hover:bg-gray-200 cursor-pointer"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-chevron-left-icon lucide-chevron-left"
          >
            <path d="m15 18-6-6 6-6" />
          </svg>
        </button>
        <button
          class="button-next absolute z-10 top-1/2 right-1 transform -translate-y-1/2 text-[#366C90] bg-gray-100 shadow-md p-1 rounded-full hover:bg-gray-200 cursor-pointer"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-chevron-right-icon lucide-chevron-right"
          >
            <path d="m9 18 6-6-6-6" />
          </svg>
        </button>
      </Swiper>

      <div class="mt-1">
        <button
          class="py-1 px-2 border-2 uppercase cursor-pointer hover:scale-95 transition-all"
        >
          Ver Todos
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper/modules";

// Import Swiper CSS
import "swiper/css";
import "swiper/css/navigation";

const kimonos = [
  {
    title: "Kimono Masculino Flow JiuJitsu GI Branco",
    price: "299,99",
    images: [
      new URL("@/assets/img/kimonosMen/kimono-branco.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Branca",
    price: "79,99",
    images: [
      new URL("@/assets/img/rashguardMen/rash-branca.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "Kimono Masculino Flow JiuJitsu GI Preto",
    price: "299,99",
    images: [
      new URL("@/assets/img/kimonosMen/kimono-preto.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Preta",
    price: "79,99",
    images: [
      new URL("@/assets/img/rashguardMen/rash-preta.png", import.meta.url).href,
    ],
  },
  {
    title: "Kimono Masculino Flow JiuJitsu GI Azul",
    price: "299,99",
    images: [
      new URL("@/assets/img/kimonosMen/kimono-azul.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Marrom",
    price: "79,99",
    images: [
      new URL("@/assets/img/rashguardMen/rash-marrom.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Azul",
    price: "79,99",
    images: [
      new URL("@/assets/img/rashguardMen/rash-azul.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Roxa",
    price: "79,99",
    images: [
      new URL("@/assets/img/rashguardMen/rash-roxa.png", import.meta.url).href,
    ],
  },
];
</script>