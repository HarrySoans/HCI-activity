<template>
    <div class="max-w-6xl mx-auto p-6">
      <h1 class="text-4xl font-bold text-center mb-6">Car Gallery</h1>
      
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <div v-for="car in cars" :key="car.id" class="bg-white rounded-lg shadow-md overflow-hidden">
          <img :src="car.image" :alt="car.name" class="w-full h-48 object-cover">
          <div class="p-4">
            <h2 class="text-lg font-semibold">{{ car.name }}</h2>
            <p class="text-gray-600">{{ car.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "GalleryPage",
    data() {
      return {
        cars: [
          { id: 1, name: "Ferrari LaFerrari", image: "LaFerrari_in_Beverly_Hills_(14563979888).jpg", description: "A hybrid supercar with a V12 engine." },
          { id: 2, name: "Lamborghini Aventador", image: "aven_gate_s_02_m.webp", description: "An iconic Italian sports car." },
          { id: 3, name: "Porsche 911", image: "0840_nevada_coupe_u-crane_AKOS0607_edit_V03-sky.jpg", description: "A timeless classic with unmatched performance." },
          { id: 4, name: "Tesla Roadster", image: "Tesla-Roadster-103.jpg.avif", description: "An all-electric supercar with extreme acceleration." },
          { id: 5, name: "Bugatti Chiron", image: "Bugatti_Chiron_1.jpg", description: "A high-performance hypercar with 1500 horsepower." }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  </style>
  