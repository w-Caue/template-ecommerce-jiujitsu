<template>
  <section
    class="flex flex-col sm:flex-row justify-center items-start gap-7 mt-10"
  >
    <router-link to="/masculino/gi" class="cursor-hover">
      <div class="relative flex flex-col items-center justify-center">
        <img
          src="../assets/img/kimonos-masculino.png"
          class="object-cover w-full h-96 rounded-sm"
          alt="todos os kimonos adultos"
        />
        <h1 class="absolute bottom-4 text-2xl">Kimonos Masculino</h1>
      </div>
    </router-link>

    <router-link to="/feminino/gi" class="cursor-hover">
      <div class="relative flex flex-col items-center justify-center">
        <img
          src="../assets/img/kimonos-femininos.png"
          class="object-cover w-full h-96 rounded-sm"
          alt="todos os kimonos femininos"
        />
        <h1 class="absolute bottom-4 text-2xl">Kimonos Feminino</h1>
      </div>
    </router-link>

    <router-link to="/kids/gi" class="cursor-hover">
      <div class="relative flex flex-col items-center justify-center">
        <img
          src="../assets/img/kimonos-kids.png"
          class="object-cover w-full h-96 rounded-sm"
          alt="todos os kimonos kids"
        />
        <h1 class="absolute bottom-4 text-2xl">Kimonos Kids</h1>
      </div>
    </router-link>
  </section>
</template>

<script>
</script>