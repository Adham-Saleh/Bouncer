<template lang="pug">
    main(class="overflow-hidden max-w-none")
      .container.flex.items-center.w-full.justify-center.mt-5(class="h-[650px] max-w-none bg-gradient-to-r from-[#FF4858] from-[#AE5DD0] to-[#8F65FF]")
          Slider(:items="sliderItems" leftBtn="LeftArr" rightBtn="RightArr")
</template>

<script setup lang="ts">
const sliderItems = ref([
  {
    image: "public/images/iphone.png",
    leftContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX 1</h2><p class="max-w-[320px] text-white font-light text-[18px]">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
    //   rightContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX</h2><p class="max-w-[320px] text-white font-light">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
  },
  {
    image: "public/images/phone.png",
    leftContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX 2</h2><p class="max-w-[320px] text-white font-light text-[18px]">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
    //   rightContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX</h2><p class="max-w-[320px] text-white font-light">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
  },
]);
</script>

<style scoped></style>
