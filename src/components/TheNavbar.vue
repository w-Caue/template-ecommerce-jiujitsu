<template>
  <nav
    class="fixed z-40 w-full top-0 flex justify-between items-center bg-white shadow-xs py-2 px-10"
  >
    <div class="sm:hidden">
      <button>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="size-6"
        >
          <path d="M4 5h16" />
          <path d="M4 12h16" />
          <path d="M4 19h16" />
        </svg>
      </button>
    </div>

    <router-link to="/">
      <img class="w-9 sm:w-12" src="../assets/logo.svg" alt="logo" />
    </router-link>

    <div class="relative hidden sm:flex flex-col items-center w-1/2">
      <ul class="sm:flex items-center gap-4 hidden h-full">
        <li
          v-on:mouseover="menuMasculino = true"
          v-on:mouseleave="menuMasculino = false"
        >
          <router-link to="/masculino" class="flex">
            Masculino
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-5"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="m6 9 6 6 6-6" />
            </svg>
          </router-link>
        </li>
        <li
          v-on:mouseover="menuFeminino = true"
          v-on:mouseleave="menuFeminino = false"
        >
          <router-link to="/feminino" class="flex">
            Feminino
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-5"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="m6 9 6 6 6-6" />
            </svg>
          </router-link>
        </li>
        <li v-on:mouseover="menuKids = true" v-on:mouseleave="menuKids = false">
          <router-link to="/kids" class="flex">
            Kids
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-5"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="m6 9 6 6 6-6" />
            </svg>
          </router-link>
        </li>
      </ul>

      <div
        v-show="menuMasculino"
        v-on:mouseover="menuMasculino = true"
        v-on:mouseleave="menuMasculino = false"
        class="absolute top-5 z-50 flex items-start gap-5 bg-white border border-gray-200 rounded-sm w-3/4"
      >
        <div class="py-4 px-3 text-start">
          <router-link to="/masculino/gi" class="text-md hover:text-blue-500">
            Kimonos
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link
                to="/masculino/gi/kimono"
                class="hover:text-blue-500"
              >
                Todos os Kimonos
              </router-link>
            </li>
          </ul>
        </div>
        <div class="py-4 px-3 text-start">
          <router-link
            to="/masculino/no-gi"
            class="text-md hover:text-blue-500"
          >
            No-Gi
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link
                to="/masculino/no-gi/rashguard"
                class="hover:text-blue-500"
              >
                Rashguard
              </router-link>
            </li>
            <li>
              <router-link
                to="/masculino/no-gi/bermuda"
                class="hover:text-blue-500"
              >
                Bermuda
              </router-link>
            </li>
          </ul>
        </div>
        <div class="py-4 px-3 text-start">
          <router-link
            to="/masculino/roupas"
            class="text-md hover:text-blue-500"
          >
            Roupas
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link
                to="/masculino/roupas/camisetas"
                class="hover:text-blue-500"
              >
                Camisetas
              </router-link>
            </li>
          </ul>
        </div>
      </div>

      <div
        v-show="menuFeminino"
        v-on:mouseover="menuFeminino = true"
        v-on:mouseleave="menuFeminino = false"
        class="absolute top-5 z-50 flex items-start gap-5 bg-white border border-gray-200 rounded-sm w-96"
      >
        <div class="py-4 px-3 text-start">
          <router-link to="/feminino/gi" class="text-md hover:text-blue-500">
            Kimonos
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link to="/feminino/gi/kimono" class="hover:text-blue-500">
                Todos os Kimonos
              </router-link>
            </li>
          </ul>
        </div>
        <div class="py-4 px-3 text-start">
          <router-link to="/feminino/no-gi" class="text-md hover:text-blue-500">
            No-Gi
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link
                to="/feminino/no-gi/rashguard"
                class="hover:text-blue-500"
              >
                Rashguard
              </router-link>
            </li>
            <li>
              <router-link
                to="/feminino/no-gi/bermuda"
                class="hover:text-blue-500"
              >
                Bermuda
              </router-link>
            </li>
          </ul>
        </div>
      </div>

      <div
        v-show="menuKids"
        v-on:mouseover="menuKids = true"
        v-on:mouseleave="menuKids = false"
        class="absolute top-5 z-50 flex items-start gap-5 bg-white border border-gray-200 rounded-sm w-72"
      >
        <div class="py-4 px-3 text-start">
          <router-link to="/kids/gi" class="text-md hover:text-blue-500">
            Kimonos
          </router-link>

          <ul class="mt-5 font-semibold text-xs space-y-3">
            <li>
              <router-link to="/kids/gi/kimono" class="hover:text-blue-500">
                Todos os Kimonos
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="flex items-center">
      <ul class="flex items-center sm:gap-8">
        <li class="hidden sm:block">
          <button>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="size-7"
            >
              <path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2" />
              <circle cx="12" cy="7" r="4" />
            </svg>
          </button>
        </li>
        <li>
          <button>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="size-7"
            >
              <circle cx="8" cy="21" r="1" />
              <circle cx="19" cy="21" r="1" />
              <path
                d="M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12"
              />
            </svg>
          </button>
        </li>
      </ul>
    </div>
  </nav>

  <router-view />
</template>

<script setup>
import { ref } from "vue";

const menuMasculino = ref(false);
const menuFeminino = ref(false);
const menuKids = ref(false);
</script>