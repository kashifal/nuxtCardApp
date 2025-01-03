<template>
    <div class="fixed inset-0 bg-black/50 flex justify-center items-center" @click.self="$emit('close')">
        <div class="bg-white p-3 sm:p-4 md:p-5 rounded-lg h-[90vh] overflow-auto w-[95%] sm:w-4/5 max-w-[600px]">
            <!-- Header section -->
            <div class="flex flex-col sm:flex-row justify-between">
                <div class="flex items-center gap-2">
                    <h2 class="text-[24px] sm:text-[28px] md:text-[32px] text-[#025144]">Second Line</h2>
                   
                </div>
                <p class="text-[8px] sm:text-[9px] md:text-[10px] text-[#C0C0C0] mt-2 sm:mt-[20px]">Last updated: Mon 30. Dec 2024</p>
            </div>
            <p class="text-[#025144] rounded-full py-[2px] text-[8px] sm:text-[9px] md:text-[10px] text-center tracking-wider bg-[#D9D9D9] w-[40px] sm:w-[45px] md:w-[50px]">
                        Two
                    </p>

            <!-- First row of images -->
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-2 sm:gap-2.5 mb-3 sm:mb-4 w-[90%]  md:mb-5 mt-4">
                <div v-for="i in 5" :key="`first-${i}`"
                    class="bg-white rounded-lg py-1 sm:py-2 flex flex-col justify-center w-full border-[0.5px] border-[#025144]">
                    <img src="/placeholder.png" alt="Placeholder" class="mx-auto  rounded" />
                    <p class="text-[8px]  text-[#C0C0C0] mx-2">
                        {{ i === 1 ? 'One' : i === 2 ? 'Two' : i === 3 ? 'Three' : i === 4 ? 'Four' : 'Five' }}
                    </p>
                    <p class="text-[10px] text-[#025144]  mx-2">
                        {{ i === 1 ? 'One' : i === 2 ? 'Two' : i === 3 ? 'Three' : i === 4 ? 'Four' : 'Five' }}
                    </p>
                </div>
            </div>

            <!-- Red bordered section -->
            <div class="border border-[#941100] p-2 sm:p-2.5 my-3 sm:my-4 md:my-5 flex">
                <div class="flex flex-col">
                    <img src="/placeholder.png" alt="Placeholder" class="h-[60px] w-[60px] sm:h-[70px] sm:w-[70px] md:h-[80px] md:w-[80px] rounded" />
                    <p class="text-[8px] sm:text-[9px] md:text-[10px] text-[#C0C0C0] mx-1">Six</p>
                    <p class="text-[9px] sm:text-[10px] md:text-[12px] text-[#025144] mx-1">Six</p>
                </div>
                <div class="ml-[15px] sm:ml-[20px] md:ml-[30px]">
                    <p class="text-[10px] sm:text-[11px] md:text-[12px] text-[#C0C0C0]">description</p>
                    <p class="text-[12px] sm:text-[13px] md:text-[14px] text-[#025144]">This is the sixth item in the list</p>
                    <p class="text-[10px] sm:text-[11px] md:text-[12px] text-[#C0C0C0]">error details</p>
                    <p class="text-[12px] sm:text-[13px] md:text-[14px] text-[#025144]">Response from the server</p>
                </div>
            </div>

            <div class="border-2  p-2 sm:p-2.5 my-3 sm:my-4 md:my-5 flex">
                <div class="flex flex-col">
                    <img src="/placeholder.png" alt="Placeholder" class="h-[60px] w-[60px] sm:h-[70px] sm:w-[70px] md:h-[80px] md:w-[80px] rounded" />
                    <p class="text-[8px] sm:text-[9px] md:text-[10px] text-[#C0C0C0] mx-1">Seven</p>
                    <p class="text-[9px] sm:text-[10px] md:text-[12px] text-[#025144] mx-1">Seven</p>
                </div>
                <div class="ml-[15px] sm:ml-[20px] md:ml-[30px]">
                    <p class="text-[10px] sm:text-[11px] md:text-[12px] text-[#C0C0C0]">description</p>
                    <p class="text-[12px] sm:text-[13px] md:text-[14px] text-[#025144]">This is the seven item from the list</p>
                </div>
            </div>


            <div class="border-2  p-2 sm:p-2.5 my-3 sm:my-4 md:my-5 flex">
                <div class="flex flex-col">
                    <img src="/placeholder.png" alt="Placeholder" class="h-[60px] w-[60px] sm:h-[70px] sm:w-[70px] md:h-[80px] md:w-[80px] rounded" />
                    <p class="text-[8px] sm:text-[9px] md:text-[10px] text-[#C0C0C0] mx-1">Eight</p>
                    <p class="text-[9px] sm:text-[10px] md:text-[12px] text-[#025144] mx-1">Eight</p>
                </div>
                <div class="ml-[15px] sm:ml-[20px] md:ml-[30px]">
                    <p class="text-[10px] sm:text-[11px] md:text-[12px] text-[#C0C0C0]">description</p>
                    <p class="text-[12px] sm:text-[13px] md:text-[14px] text-[#025144]">This is the eight item from the list</p>
                </div>
            </div>

            <!-- Additional image rows -->
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-2 sm:gap-2.5 mb-3 sm:mb-4 w-[90%]  md:mb-5 mt-4">
                <div v-for="i in 3" :key="`first-${i}`"
                    class="bg-white rounded-lg py-1 sm:py-2 flex flex-col justify-center w-full border-[0.5px] border-[#025144]">
                    <img src="/placeholder.png" alt="Placeholder" class="mx-auto  rounded" />
                    <p class="text-[8px]  text-[#C0C0C0] mx-2">
                        {{ i === 1 ? 'One' : i === 2 ? 'Two' : i === 3 ? 'Three' : i === 4 ? 'Four' : 'Five' }}
                    </p>
                    <p class="text-[10px] text-[#025144]  mx-2">
                        {{ i === 1 ? 'One' : i === 2 ? 'Two' : i === 3 ? 'Three' : i === 4 ? 'Four' : 'Five' }}
                    </p>
                </div>
            </div>

            <!-- Submit button -->
            <div class="text-right mt-3 sm:mt-4 md:mt-5">
                <button 
                    @click="$emit('close')" 
                    class="bg-[#00ff00] text-white px-4 sm:px-5 py-2 sm:py-2.5 text-[12px] sm:text-[14px] rounded-full cursor-pointer"
                >
                    CLOSE
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
defineProps({
    selectedImage: {
        type: Object,
        required: true
    }
});

defineEmits(['close']);
</script>
