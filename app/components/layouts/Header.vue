<script setup>
const menuItems = [
  { name: "Projets", path: "#projects" },
  { name: "Process", path: "#process" },
  { name: "À propos", path: "#about" },
];
</script>
<template>
  <header
    class="fixed top-0 left-0 w-full flex justify-center py-6 z-50 pointer-events-none"
  >
    <nav
      class="pointer-events-auto py-2 px-2 rounded-full bg-white/80 backdrop-blur-md border border-gray-100 shadow-xl"
    >
      <ul class="flex items-center gap-1 sm:gap-4">
        <li v-for="item in menuItems" :key="item.name">
          <NuxtLink
            :to="item.path"
            class="px-4 py-2 text-sm font-medium text-gray-600 hover:text-black transition-colors duration-300 rounded-full"
          >
            {{ item.name }}
          </NuxtLink>
        </li>

        <li>
          <NuxtLink
            to="/cv-maurice.pdf"
            target="_blank"
            class="bg-black text-white px-5 py-2.5 rounded-full text-sm font-bold shadow-lg transition-all hover:bg-gray-800 hover:scale-105 active:scale-95 flex items-center gap-2"
          >
            <span>Mon CV</span>
            <span class="text-[10px] bg-white/20 px-1.5 py-0.5 rounded italic"
              >PDF</span
            >
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>

  <div class="h-20"></div>
</template>
