<template>
  <div class="home">
    <TheHeader />

    <main class="mx-9">
      <FirstMenu />
      <FirstCarousel />
      <SecondMenu />
      <SecondCarousel />
      <ThirdMenu />
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import FirstCarousel from '@/components/FirstCarousel.vue';
import FirstMenu from '@/components/FirstMenu.vue';
import SecondCarousel from '@/components/SecondCarousel.vue';
import SecondMenu from '@/components/SecondMenu.vue';
import TheHeader from '@/components/TheHeader.vue';
import ThirdMenu from '@/components/ThirdMenu.vue';

export default {
  name: 'HomeView',
  components: {
    TheHeader,
    FirstMenu,
    FirstCarousel,
    SecondMenu,
    SecondCarousel,
    ThirdMenu
  }
}
</script>
