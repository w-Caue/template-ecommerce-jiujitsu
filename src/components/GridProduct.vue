<template>
  <section>
    <div class="grid sm:grid-cols-3 gap-5">
      <div
        v-for="(product, index) in filteredProducts"
        :key="index"
        class="bg-white w-full mx-auto cursor-pointer"
      >
        <img
          :src="product.images"
          :alt="product.name"
          class="w-full h-96 object-cover"
          loading="lazy"
        />

        <div class="relative text-start py-4">
          <h1 class="text-md font-semibold text-[#393939]">
            {{ product.title }}
          </h1>

          <h2 class="text-md mt-1">R${{ product.price }}</h2>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { computed } from 'vue';
import { useRoute } from 'vue-router'

const route = useRoute();

const category = computed(() => route.params.category)
const type = computed(() => route.params.type)
const group = computed(() => route.params.group)

const products = [
  {
    title: "Kimono Masculino Flow JiuJitsu GI Branco",
    price: "299,99",
    category: 'masculino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-branco.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Branca",
    price: "79,99",
    category: 'masculino',
    type: 'no-gi',
    group: 'rashguard',
    images: [
      new URL("@/assets/img/rashguardMen/rash-branca.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "Kimono Masculino Flow JiuJitsu GI Preto",
    price: "299,99",
    category: 'masculino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-preto.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Preta",
    price: "79,99",
    category: 'masculino',
    type: 'no-gi',
    group: 'rashguard',
    images: [
      new URL("@/assets/img/rashguardMen/rash-preta.png", import.meta.url).href,
    ],
  },
  {
    title: "Kimono Masculino Flow JiuJitsu GI Azul",
    price: "299,99",
    category: 'masculino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-azul.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Marrom",
    price: "79,99",
    category: 'masculino',
    type: 'no-gi',
    group: 'rashguard',
    images: [
      new URL("@/assets/img/rashguardMen/rash-marrom.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Azul",
    price: "79,99",
    category: 'masculino',
    type: 'no-gi',
    group: 'rashguard',
    images: [
      new URL("@/assets/img/rashguardMen/rash-azul.png", import.meta.url).href,
    ],
  },
  {
    title: "RashGuard Masculina Flow NOGI Manga Roxa",
    price: "79,99",
    category: 'masculino',
    type: 'no-gi',
    group: 'rashguard',
    images: [
      new URL("@/assets/img/rashguardMen/rash-roxa.png", import.meta.url).href,
    ],
  },
  {
    title: "Kimono Feminino Flow JiuJitsu GI Branco",
    price: "299,99",
    category: 'feminino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-branco.png", import.meta.url)
        .href,
    ],
  },
  {
    title: "Kimono Feminino Flow JiuJitsu GI Preto",
    price: "299,99",
    category: 'feminino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-preto.png", import.meta.url).href,
    ],
  },
  {
    title: "Kimono Femino Flow JiuJitsu GI Azul",
    price: "299,99",
    category: 'feminino',
    type: 'gi',
    group: 'kimono',
    images: [
      new URL("@/assets/img/kimonosMen/kimono-azul.png", import.meta.url).href,
    ],
  },
];

const filteredProducts = computed(() => {
  return products.filter(p =>
    (!category.value || p.category === category.value) &&
    (!type.value || p.type === type.value) &&
    (!group.value || p.group === group.value)
  )
})
</script>