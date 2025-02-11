<template lang="pug">
    nav.border-b-2.w-full.flex(class="py-[24px] border-[#FAFAFB] justify-between px-[10px] md:px-[150px] md:justify-center")
        .logo(class="black md:hidden")
            h2 BOUNCER
        .mobile-menu-btn(class="block md:hidden")   
            button 
                Icon(name="MenuBtn")
        .container.flex.justify-between(class="hidden md:flex")
            .flex.gap-2
                select 
                    option(value="en" selected) EN
                    option(value="ar") AR
                select 
                    option(value="usd" selected) USD
                    option(value="egp") EGP
            .flex.gap-8
                button.flex.gap-1.items-center
                    Icon(name="Profile")
                    span My profile
                button.flex.gap-1.items-center
                    Icon(name="Cart")
                    span 0 Items
                    span(class="text-[#262626]") $0.00
                button
                    Icon(name="Search")
    .logo.flex.justify-center.items-center.flex-col.gap-3.mt-3
        h3.font-bold.tracking-widest(class="text-[#FF4252] lg:text-[36px] text-[24px] uppercase") Bouncer
        ul.flex.gap-8.flex-wrap(class="justify-center")
            li(v-for="item in menuItems")
                NuxtLink.font-semibold.uppercase(:to="`${item?.link}`" class="text-[14px]") {{ item?.name }}
</template>

<script setup lang="ts">
const menuItems = [
  {
    name: "Home",
    link: "/",
  },
  {
    name: "Store",
    link: "/store",
  },
  {
    name: "Iphone",
    link: "/iphone",
  },
  {
    name: "Ipad",
    link: "/ipad",
  },
  {
    name: "Macbook",
    link: "/macbook",
  },
  {
    name: "Accesories",
    link: "/accesories",
  },
];
</script>

<style scoped></style>
