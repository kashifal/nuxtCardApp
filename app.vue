<template>
  <div class="min-h-screen bg-gray-100 p-8">
    <!-- Header section -->
    <div class="flex items-center justify-between mb-8">
      <h1 class="text-2xl font-bold">NAME OF APP</h1>
      <div class="flex gap-4">
        <button class="p-2 hover:bg-gray-200 rounded-full">
          <span class="sr-only">Notifications</span>
          🔔
        </button>
        <button class="p-2 hover:bg-gray-200 rounded-full">
          <span class="sr-only">Menu</span>
          ⋮
        </button>
      </div>
    </div>

    <!-- Search bar -->
    <div class="relative mb-8">
      <input 
        type="text" 
        placeholder="Search here..." 
        class="w-full p-3 rounded-lg bg-white shadow-sm"
      >
    </div>

    <!-- Image grid -->
    <div class="space-y-8">
      <div v-for="(row, rowIndex) in imageRows" :key="rowIndex">
        <h2 class="text-lg font-semibold mb-4">Row {{ rowIndex + 1 }}</h2>
        <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-4">
          <div v-for="(image, imageIndex) in row" :key="imageIndex" 
               class="aspect-square bg-white rounded-lg shadow-sm p-2">
            <img 
              :src="image.url" 
              :alt="image.title"
              class="w-full h-full object-cover rounded"
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const imageRows = [
  // First row
  [
    { url: '/path/to/image1.jpg', title: 'One' },
    { url: '/path/to/image2.jpg', title: 'Two' },
    { url: '/path/to/image3.jpg', title: 'Three' },
    { url: '/path/to/image4.jpg', title: 'Four' },
    { url: '/path/to/image5.jpg', title: 'Five' },
    { url: '/path/to/image6.jpg', title: 'Six' },
  ],
  // Second row
  [
    { url: '/path/to/image7.jpg', title: 'Seven' },
    { url: '/path/to/image8.jpg', title: 'Eight' },
    { url: '/path/to/image9.jpg', title: 'Nine' },
    { url: '/path/to/image10.jpg', title: 'Ten' },
    { url: '/path/to/image11.jpg', title: 'Eleven' },
  ],
  // Third row
  [
    { url: '/path/to/image12.jpg', title: 'One' },
    { url: '/path/to/image13.jpg', title: 'Two' },
    { url: '/path/to/image14.jpg', title: 'Three' },
    { url: '/path/to/image15.jpg', title: 'Four' },
    { url: '/path/to/image16.jpg', title: 'Five' },
  ],
]
</script>