<template>
  <section
    class="flex flex-col sm:flex-row justify-center items-start gap-10 mt-22"
  >
    <router-link to="/masculino/no-gi" class="cursor-hover">
      <div class="relative flex flex-col items-center justify-center">
        <img
          src="../assets/img/bermudas.png"
          class="object-cover w-full h-96 rounded-sm"
          alt="todos os kimonos adultos"
        />
        <h1 class="absolute bottom-1 text-2xl">No-gi Masculino</h1>
      </div>
    </router-link>

    <router-link to="/feminino/no-gi" class="cursor-hover">
      <div class="relative flex flex-col items-center justify-center">
        <img
          src="../assets/img/rashguard.png"
          class="object-cover w-full h-96 rounded-sm"
          alt="todos os kimonos adultos"
        />
        <h1 class="absolute bottom-1 text-2xl">No-gi feminino</h1>
      </div>
    </router-link>
  </section>
</template>

<script>
</script>