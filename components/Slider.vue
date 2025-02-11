<template lang="pug">
    .slider.flex.justify-between.items-center(class="gap-[140px] px-[30px]")
        aside
            button
                Icon(:name="items?.leftBtn")

        main.flex.items-center(class="gap-[100px]")
            span.flex.flex-col.justify-between(v-html="items?.leftContent" class="gap-[50px]") 
            
            img(:src="`/_nuxt/${items?.imgs[0]}`" class="max-w-[420px]")

            span.flex.flex-col.justify-between(v-html="items?.rightContent" class="gap-[50px]")

        aside 
            button
                Icon(:name="items?.rightBtn")
</template>

<script setup lang="ts">
// imgs: {
//     type: Array,
//   },
//   leftContent: {
//     type: String,
//   },
//   rightContent: {
//     type: String,
//   },
//   leftBtn: {
//     type: String,
//   },
//   rightBtn: {
//     type: String,
//   },

// items will be an array which will hold all properties above

const props = defineProps({
  items: {
    type: Object,
  },
});
</script>

<style scoped></style>
