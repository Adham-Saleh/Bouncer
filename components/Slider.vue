<template lang="pug">
    .slider.flex.flex-col(class="lg:flex-row justify-between items-center gap-10 lg:gap-[140px] px-[50px]")
      aside.hidden(class="lg:block")
          button(:disabled="currentSlide === 0" @click="handleSlider('decrement')")
              Icon(:name="leftBtn")

      main.flex.overflow-x-auto.flex-wrap.shrink-0.relative.m-auto.max-w-screen
          .content.flex.flex-col.flex-nowrap(v-for="item, idx in items" class="lg:flex-row items-center flex-wrap gap-10 lg:gap-[100px] text-center lg:text-left" :class="{'hidden': idx !== currentSlide}")
            span.flex.flex-col.justify-between(v-html="item?.leftContent" class="gap-6 lg:gap-[50px]") 
            
            img(:src="`/_nuxt/${item?.image}`" class="max-w-[250px] lg:max-w-[420px]")
            
            span.flex.flex-col.justify-between(v-html="item?.rightContent" class="gap-6 lg:gap-[50px]")

      aside.hidden(class="lg:block")
        
          button(:disabled="currentSlide === (items?.length - 1)" @click="handleSlider('increment')")
              Icon(:name="rightBtn")

</template>

<script setup lang="ts">
const currentSlide = ref(0);

const { items } = defineProps({
  items: {
    type: Array,
  },
  leftBtn: {
    type: String,
  },
  rightBtn: {
    type: String,
  },
});

const handleSlider = function (method: string) {
  if (method === "increment") {
    currentSlide.value += 1;
  } else {
    currentSlide.value -= 1;
  }
};
</script>

<style scoped></style>
