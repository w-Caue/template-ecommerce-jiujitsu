<template>
  <section class="mt-22 mx-9">
    <nav class="flex mb-6" aria-label="Breadcrumb">
      <ol
        class="inline-flex items-center space-x-1 md:space-x-2 rtl:space-x-reverse"
      >
        <li class="inline-flex items-center">
          <router-link
            to="/"
            class="inline-flex items-center text-xs hover:text-[#366C90]"
          >
            Home
          </router-link>
        </li>

        <li aria-current="page">
          <div class="flex items-center">
            <svg
              class="rtl:rotate-180 w-3 h-3 text-gray-400 mx-1"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 6 10"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="m1 9 4-4-4-4"
              />
            </svg>
            <span class="ms-1 text-xs text-gray-500 md:ms-2">{{
              $route.params.category
            }}</span>
          </div>
        </li>
      </ol>
    </nav>

    <div class="grid sm:grid-cols-5 sm:gap-5">
      <div>
        <FilterProduct />
      </div>

      <div class="sm:col-span-4">
        <GridProduct />
      </div>
    </div>
  </section>
</template>

<script>
import FilterProduct from "@/components/FilterProduct.vue";
import GridProduct from "@/components/GridProduct.vue";

export default {
  name: "CategoryView",
  components: {
    GridProduct,
    FilterProduct,
  },
};
</script>