<template lang="pug">
    main(class="overflow-hidden max-w-none")
      section.container.flex.items-center.w-full.justify-center.mt-5(class="h-[650px] max-w-none bg-gradient-to-r from-[#FF4858] from-[#AE5DD0] to-[#8F65FF]")
          Slider(:items="sliderItems" leftBtn="LeftArr" rightBtn="RightArr")

      section(class="py-[50px]")

        h1.text-center(class="text-[24px] uppercase") Best selling
        ul.flex.gap-8.flex-wrap(class="justify-center my-[25px]")
              li(v-for="item in tabs" :class="{'text-blue-400 border-b-[4px] border-blue-400': activeTab === item}")
                  button.font-semibold.uppercase(class="text-[14px]" @click="handleTabChange(item)") {{ item }}

        main(class="mt-[35px] mx-[10px] md:mx-[100px]")
          .grid(class="gap-[24px] md:grid-cols-2 lg:grid-cols-4")
            .products.flex.flex-col.justify-center.items-center(v-for="product in 8" class="gap-[8px] max-width-[100%] border rounded-[10px] py-[10px]")
              img(src="../public/images/phone.png" class="max-w-[100%] lg:max-w-[200px]" v-if="!hovering" @mouseover="hovering = true")
              .actions.flex.gap-2(v-else @mouseout="hovering = false")
                button info 
                button share
              span.font-medium iPhone XSZ
              .rates.flex.flex-row.gap-1
                .star(v-for="star in 4")
                  Icon(name="StarFill")
                .star(v-for="star in 1")
                  Icon(name="StarEmpty")
              .price.flex.gap-2 
                .sale-price.text-red-400
                  | 499$  
                .og-price.text-gray-400.line-through
                  | 599$  
          .load-more.flex.justify-center(class="mt-[35px]")
            button(class="text-blue-400 border-b-[4px] border-blue-400") Load more

      section(class="py-[50px] px-[10px] md:px-[100px] bg-blue-400 text-white")
        .flex.justify-between.items-center(class="md:.overflow-hidden")
          .flex.flex-col(class="gap-[35px]")
            header(class="space-y-[10px]") 
              h1(class="text-[48px]") iPhone 6 plus 
              span.font-light(class="text-[24px]") Performance and shit
            button(class="text-white border-b-[4px] border-white flex justify-start max-w-[80px]") Shop now
          img(src="../public/images/phone.png" class="max-w-[250px] hidden md:block lg:max-w-[600px]")

      section(class="py-[50px] px-[10px] lg:px-[100px]")
        .flex.items-center.justify-center.flex-wrap(class="gap-[25px]")
          .flex.flex-col.text-center.items-center(class="gap-[30px]")
            Icon(name="Shipping")
            h1(class="text-[18px] uppercase font-medium") Free Shipping
            span.font-light(class="text-[14px] max-w-[330px]") Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor minim veniam, quis nostrud  reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
          .flex.flex-col.text-center.items-center(class="gap-[30px]")
            Icon(name="Refund")
            h1(class="text-[18px] uppercase font-medium") 100% refund
            span.font-light(class="text-[14px] max-w-[330px]") Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor minim veniam, quis nostrud  reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
          .flex.flex-col.text-center.items-center(class="gap-[30px]")
            Icon(name="Support")
            h1(class="text-[18px] uppercase font-medium") Support 24/7
            span.font-light(class="text-[14px] max-w-[330px]") Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor minim veniam, quis nostrud  reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur

      section(class="py-[50px] px-[10px] lg:px-[100px]")
        h1.text-center(class="text-[24px] uppercase") LATEST NEWS
        .grid(class="mt-[35px] md:grid-cols-2 lg:grid-cols-3")
          .flex.flex-wrap(class="gap-[20px]" v-for="i in 3")
            img(src="../public/images/phone.png" class="max-w-[200px]")
            .flex.flex-col(class="gap-[8px] py-[25px]")
              span.text-gray-400.font-light 8 Jan 2000
              span.font-medium Typescript
              span(class="max-w-[203px]") Lorem Ipsum is simply dummy text of the printing and typesetting industry.


      section(class="py-[50px] px-[10px] lg:px-[100px]")
        h1.text-center(class="text-[24px] uppercase") FEATURED PRODUCTS
        .grid(class="mt-[35px] md:grid-cols-2 lg:grid-cols-3")
          .flex.flex-wrap(class="gap-[20px]" v-for="i in 3")
            img(src="../public/images/phone.png" class="max-w-[200px]")
            .flex.flex-col(class="gap-[8px] py-[25px]")
              span.font-medium Typescript
              .rates.flex.flex-row.gap-1(class="mt-[25px]")
                .star(v-for="star in 4")
                  Icon(name="StarFill")
                .star(v-for="star in 1")
                  Icon(name="StarEmpty")
              .price.flex.gap-2 
                .sale-price.text-red-400
                  | 499$  
                .og-price.text-gray-400.line-through
                  | 599$  
      
      section(class="py-[50px] px-[10px] lg:px-[100px]")
        .flex.justify-center
          input(type="text" placeholder="Search query . . ." class="lg:min-w-[480px] border px-[12px] py-[14px] placeholder:font-normal rounded-l-md focus:border-r-0 focus:outline-blue-400")
          button(class="bg-blue-400 text-white px-[12px] border-blue-400 rounded-r-md py-[14px] lg:min-w-[120px]") Search
</template>

<script setup lang="ts">
const router = useRouter();
const route = useRoute();

const sliderItems = ref([
  {
    image: "public/images/iphone.png",
    leftContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX 1</h2><p class="max-w-[320px] text-white font-light text-[18px]">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
  },
  {
    image: "public/images/phone.png",
    leftContent: `<h2 class="text-[48px] text-white font-medium">iPhoneX 2</h2><p class="max-w-[320px] text-white font-light text-[18px]">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy.</p>`,
  },
]);
const tabs = ref(["All", "Mac", "iPad", "iPhone", "iPod", "Accessories"]);

const activeTab = ref<string>((route.query.tab as string) || "All");
const hovering = ref<boolean>(false);

const handleTabChange = function (tab: string) {
  activeTab.value = tab;
  router.push({
    query: { tab },
  });
};
</script>

<style scoped></style>
