<template>
  <div class="flex justify-center mb-2 sm:hidden">
    <button
      class="flex justify-center w-full bg-gray-100 rounded-sm py-2 text-[#393939] uppercase hover:scale-95 transition-all cursor-pointer"
      x-on:click="$dispatch('open-modal-filter', { name : 'filter' })"
    >
      Filtros
    </button>
  </div>
</template>