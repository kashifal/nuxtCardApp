<template>
    <div class="flex items-center justify-between mb-8 px-[30px] bg-gray-100  py-[20px]">
        <div class="flex items-center gap-2 md:gap-4">
            <img src="/placeholder.png" alt="Logo" class="h-[56px] md:h-[72px] ">
            <h1 class="text-[16px] md:text-[34px] font-bold">NAME OF APP</h1>
        </div>
        <div class="flex gap-4">

           <img src="/home-svgrepo-com 1.png" class="h-[30px] md:h-auto" alt="">




           <img src="/apps-svgrepo-com.png" class="h-[30px] md:h-auto" alt="">

        </div>
    </div>
    <div class="p-4 sm:p-6 md:p-8 max-w-7xl mx-auto">
        <!-- Search bar -->
        <div class="mb-4 sm:mb-6 md:mb-8 flex flex-col sm:flex-row gap-4 sm:gap-2">
            <div class="w-full sm:w-[85%]">
                <input type="text" 
                    placeholder="Search here..." 
                    class="w-full p-2 sm:p-4 
                        placeholder:text-[#D5DABF] 
                        placeholder:text-lg sm:placeholder:text-2xl md:placeholder:text-[34px] 
                        bg-[#E8E9E3] 
                        pl-[20px] 
                        rounded-lg 
                        border 
                        h-[50px]  sm:h-[70px] md:h-[87px]">
            </div>

            <div class="flex items-center gap-1 sm:gap-2">
                <div class="bg-[#E8E9E3] h-[50px] sm:h-[70px] md:h-[87px] w-[60px] sm:w-[80px] md:w-[103px] flex items-center justify-center">
                    <img src="/search-svgrepo-com.png" alt="" class="w-6 sm:w-8 md:w-10">
                </div>

                <div class="bg-[#E8E9E3] h-[50px] sm:h-[70px] md:h-[87px] w-[60px] sm:w-[80px] md:w-[103px] flex items-center justify-center">
                    <img src="/alert-triangle-svgrepo-com.png" alt="" class="w-6 sm:w-8 md:w-10">
                </div>

                <div class="bg-[#E8E9E3] h-[50px] sm:h-[70px] md:h-[87px] w-[60px] sm:w-[80px] md:w-[103px] flex items-center justify-center">
                    <img src="/apps-svgrepo-com.png" alt="" class="w-6 sm:w-8 md:w-10">
                </div>

                <div class="h-[50px] sm:h-[70px] md:h-[87px] w-[60px] sm:w-[80px] md:w-[103px] flex items-center justify-center">
                    <img src="/x-circle-svgrepo-com 1.png" alt="" class="w-6 sm:w-8 md:w-10">
                </div>
            </div>
        </div>

        <!-- Image grid -->
        <div class="space-y-4 sm:space-y-6 md:space-y-8">
            <div v-for="(row, rowIndex) in imageRows" :key="rowIndex">
                <!-- Header section -->
                <div class="mb-3 sm:mb-4 w-full sm:w-auto mt-4 sm:mt-6 md:mt-[50px]">
                    <div class="flex items-center gap-2 flex-wrap sm:flex-nowrap">
                        <p class="text-[10px] sm:text-[12px] md:text-[14px] text-[#025144] font-semibold">First line</p>
                        <p class="text-[8px] sm:text-[10px] md:text-[12px] bg-[#D9D9D9] px-2 sm:px-[10px] py-1 rounded-full text-[#025144] font-semibold">one</p>
                    </div>
                    <p class="text-[8px] sm:text-[10px] md:text-[12px] text-[#C0C0C0] mt-1">Last Updated: Mon 30. Dec 2024</p>
                </div>

                <!-- Image grid -->
                <div class="grid grid-cols-1 sm:grid-cols-3 md:grid-cols-6 lg:grid-cols-11 gap-2 sm:gap-4" :class="{
                    'md:grid-cols-6': rowIndex === 0,
                    'md:grid-cols-11': rowIndex > 0
                }">
                    <div v-for="(image, imageIndex) in row" :key="imageIndex"
                        class="bg-white rounded-lg shadow-sm py-10 md:px-2 md:py-2 flex flex-col justify-center w-full"
                        :class="{
                            'border-[0.5px] border-[#025144]': imageIndex !== 0  // Add border only if not the first div
                        }">
                        <img :src="image.url" 
                            :alt="image.title" 
                            class="mx-auto object-cover  md:w-[auto] w-[40%]" />
                        <p class="text-[8px] sm:text-[9px] md:text-left md:text-[10px] mt-2 text-center">{{ image.title }}</p>
                        <p class="text-[9px] sm:text-[10px] md:text-[12px] text-[#025144] mt-1 md:text-left text-center">{{ image.title }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const imageRows = [
    // First row - 6 images
    [
        { url: '/placeholder.png', title: 'One' },
        { url: '/placeholder.png', title: 'Two' },
        { url: '/placeholder.png', title: 'Three' },
        { url: '/placeholder.png', title: 'Four' },
        { url: '/placeholder.png', title: 'Five' },
        { url: '/placeholder.png', title: 'Six' },
    ],
    // Second row - 11 images
    [
        { url: '/placeholder.png', title: 'One' },
        { url: '/placeholder.png', title: 'Two' },
        { url: '/placeholder.png', title: 'Three' },
        { url: '/placeholder.png', title: 'Four' },
        { url: '/placeholder.png', title: 'Five' },
        { url: '/placeholder.png', title: 'Six' },
        { url: '/placeholder.png', title: 'Seven' },
        { url: '/placeholder.png', title: 'Eight' },
        { url: '/placeholder.png', title: 'Nine' },
        { url: '/placeholder.png', title: 'Ten' },
        { url: '/placeholder.png', title: 'Eleven' },
    ],
    // Third row - 11 images
    [
        { url: '/placeholder.png', title: 'One' },
        { url: '/placeholder.png', title: 'Two' },
        { url: '/placeholder.png', title: 'Three' },
        { url: '/placeholder.png', title: 'Four' },
        { url: '/placeholder.png', title: 'Five' },
        { url: '/placeholder.png', title: 'Six' },
        { url: '/placeholder.png', title: 'Seven' },
        { url: '/placeholder.png', title: 'Eight' },
        { url: '/placeholder.png', title: 'Nine' },
        { url: '/placeholder.png', title: 'Ten' },
        { url: '/placeholder.png', title: 'Eleven' },
    ],
];
</script>