<template lang="pug">
    header(class="flex justify-center gap-3 mt-[50px]")
        span Home
        span /
        span Store
    
    main(class="flex justify-center gap-3 mt-8 pb-[50px] flex-wrap")
        .flex.flex-col(class="gap-[8px]")
            .flex.flex-col(class="bg-[#F6F7F8] p-[24px] rounded-[4px] gap-[16px] min-w-[270px]")
                h1(class="uppercase text-[18px]") Accessories  
                .flex.flex-col
                    ul(class="text-[14px]")
                        li.flex.justify-between 
                            span Apple Car 
                            span 3
                .flex.flex-col.gap-3 
                    ul(class="text-[14px]")
                        li.flex.justify-between.flex 
                            span Airepods and wireless
                            span 3
                .flex.flex-col.gap-3 
                    ul(class="text-[14px]") 
                        li.flex.justify-between 
                            span Apple Car 
                            span 3
            .flex.flex-col(class="bg-[#F6F7F8] p-[24px] rounded-[4px] gap-[16px] min-w-[270px]")
                h1(class="uppercase text-[18px]") price  
                .flex.flex-col
                    ul(class="text-[14px]")
                        li.flex.justify-between 
                            span Ranger 
                            span $13.99 - $25.99
                    input(type="range" class="mt-2")
            .flex.flex-col(class="bg-[#F6F7F8] p-[24px] rounded-[4px] gap-[16px] min-w-[270px]")
                h1(class="uppercase text-[18px]") color  
                .flex(class="gap-3")
                    div(class="rounded-full p-[3px] border border-blue-400 flex justify-center items-center")
                        div(class="bg-blue-400 size-[15px] rounded-full")
                    div(class="rounded-full p-[3px] flex justify-center items-center")
                        div(class="bg-red-400 size-[15px] rounded-full")
        .flex.flex-col(class="gap-8") 
            section(class=" px-[50px] py-[30px]  bg-blue-400 text-white rounded-[4px] lg:min-w-[675px]")
                .flex.justify-between.items-center(class="md:.overflow-hidden")
                    .flex.flex-col(class="gap-[35px]")
                        header(class="space-y-[10px]") 
                        h1(class="text-[48px] font-light") iPhone 8
                        span.font-light(class="text-[24px]") Performance and shit
                        button(class="text-white border-b-[4px] border-white flex justify-start max-w-[80px]") Shop now
                    div(class="lg:max-w-[250px] hidden lg:block")
                        img(src="../public/images/phone.png" class="w-full")
            section(class="flex justify-center px-[50px]")
                .container.flex.justify-between
                    .inputs.flex.gap-3
                        .sort
                            label Sort by 
                            select.border
                                option Name
                        .sort
                            label Sort by 
                            select.border 
                                option Name
                    .layout.flex.gap-3
                        .grid
                            label layout 1
                        .list
                            label layout 2
            section 
                .grid(class="gap-[24px] md:grid-cols-2 lg:grid-cols-3")
                    .products.flex.flex-col.justify-center.items-center(v-for="product in 6" class="gap-[8px] min-w-[300px] border rounded-[10px] py-[10px]")
                        div(class="max-w-[100%] lg:max-w-[200px]")
                            img(src="../public/images/phone.png" class="w-full" @mouseover="hovering = true")
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

</template>

<script setup lang="ts"></script>

<style scoped></style>
