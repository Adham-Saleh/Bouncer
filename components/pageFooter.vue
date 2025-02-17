<template lang="pug">
    div(class="px-[10px] lg:px-[100px] sticky top-0")
        .grid(class="lg:grid-cols-3 md:grid-cols-2   gap-8 py-[50px]")
            div.flex.flex-col.gap-3
                h1(class="text-[48px] text-[#c1c8ce]") Bouncer 
                span(class="text-[#22262a] font-light") Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever.Since the 1500s, when an unknown printer.
            div.flex.flex-col.gap-3
                h1(class="text-[24px]") Follow us 
                span(class="text-[#22262a] font-light") Since the 1500s, when an unknown printer took a galley of type and scrambled.
                .flex.gap-2 
                    span Facebook 
                    span twitter
            div.flex.flex-col.gap-3
                h1(class="text-[24px]") Contact us 
                span(class="text-[#22262a] font-light") My Company , 4578 Marmora Road, Glasgow D04 89GR Call us now: 0123-456-789 Email: support@whatever.com
        .divider
            hr
        .grid(class="lg:grid-cols-6 md:grid-cols-3   gap-8 py-[50px]") 
                ul(v-for="item in items" class="flex flex-col gap-2")
                    li(class="font-normal mb-6") {{ item?.title }}
                    li(v-for="link in item.links" class="cursor-pointer text-gray-600") {{ link?.title }}
        hr
        .flex.justify-between.flex-wrap(class=" py-[20px]")
            span © 2018 Ecommerce theme by www.bisenbaev.com
            .payments.flex.gap-3.flex-wrap
                span v1
                span v2
                span v3
                span v4

</template>

<script setup lang="ts">
const items = [
  {
    title: "Information",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
  {
    title: "Service",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
  {
    title: "Extra",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
  {
    title: "My account",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
  {
    title: "Userful link",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
  {
    title: "Our Offers",
    links: [
      {
        title: "About us",
        link: "/",
      },
      {
        title: "Information",
        link: "/",
      },
      {
        title: "Privacy policy",
        link: "/",
      },
      {
        title: "Terms & conditions",
        link: "/",
      },
    ],
  },
];
</script>

<style scoped></style>
