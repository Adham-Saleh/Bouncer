<template lang="pug">
    .container.flex.items-center.w-full.justify-center.mt-5(class="h-[650px] bg-gradient-to-r from-[#FF4858] from-[#AE5DD0] to-[#8F65FF]")
        Slider(:items="sliderItems")
</template>

<script setup lang="ts">
const sliderItems = ref({
  imgs: ["public/images/iphone.png"],
  leftContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX</h2><p class="max-w-[320px] text-white font-light">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
//   rightContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX</h2><p class="max-w-[320px] text-white font-light">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
  leftBtn: "LeftArr",
  rightBtn: "RightArr",
});
</script>

<style scoped></style>
