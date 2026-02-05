<script setup>
const projects = [
  {
    title: "Space tourism",
    category: "Challenge frontend mentor • Nuxt",
    image: "/images/space.jpg",
    link: "https://space-tourism-m.netlify.app",
  },
  {
    title: "Loopstudios",
    category: "Challenge frontend mentor • Nuxt",
    image: "/images/loopstudios.jpg",
    link: "https://loopstudios-landing-page-m.netlify.app",
  },
  {
    title: "Insure landing page",
    category: "Challenge frontend mentor • Nuxt",
    image: "/images/insure.jpg",
    link: "https://insure-landing-page-m.netlify.app",
  },
  {
    title: "Vous êtes ici",
    category: "Portfolio",
    image: "/images/portfolio.png",
    link: "/",
  },
];
</script>
<template>
  <section class="max-w-6xl mx-auto px-6 py-24" id="projects">
    <div class="text-center mb-16">
      <div
        class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-green-50 text-green-600 font-medium text-sm mb-4"
      >
        <span class="h-2 w-2 rounded-full bg-green-400"></span>
        Mes réalisations
      </div>
      <h2 class="font-bold text-4xl md:text-5xl text-gray-900">
        Un aperçu de mon travail
      </h2>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="group bg-white rounded-3xl shadow-sm border border-gray-100 overflow-hidden hover:shadow-2xl transition-all duration-500"
      >
        <div class="relative overflow-hidden bg-gray-100 p-4">
          <div class="overflow-hidden rounded-2xl">
            <img
              class="w-full h-64 object-cover transition-transform duration-700 group-hover:scale-110"
              :src="project.image"
              :alt="project.title"
            />
          </div>
        </div>

        <div class="p-8">
          <div class="flex justify-between items-center">
            <div>
              <h3 class="text-2xl font-bold text-gray-900 mb-1">
                {{ project.title }}
              </h3>
              <p class="text-gray-500 text-sm italic">{{ project.category }}</p>
            </div>

            <NuxtLink
              :to="project.link"
              target="_blank"
              class="flex items-center gap-2 bg-black text-white px-5 py-2.5 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors"
            >
              Voir le site
              <span class="text-xs">↗</span>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
