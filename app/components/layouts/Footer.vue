<script setup>
const navLinks = [
  { name: "Projets", to: "#projects" },
  { name: "Mon process", to: "#" },
  { name: "À propos", to: "#about" },
];

const socialLinks = [
  { name: "Linkedin", to: "#" },
  { name: "Github", to: "#" },
  { name: "Email", to: "mailto:votre@email.com" },
];
</script>

<template>
  <footer class="bg-black text-white pt-20 pb-10">
    <div class="max-w-6xl mx-auto px-6">
      <div class="flex flex-col md:flex-row justify-between gap-12 pb-16">
        <div class="flex flex-col gap-3">
          <span class="font-bold text-3xl tracking-tighter"
            >Maurice Mumbere</span
          >
          <span class="text-green-400 font-medium">Développeur Fullstack</span>
          <p class="text-white/50 max-w-xs text-sm mt-2">
            Spécialisé dans la création d'expériences numériques performantes et
            sur-mesure.
          </p>
        </div>

        <div class="grid grid-cols-2 gap-12 md:gap-24">
          <nav>
            <h2
              class="font-bold mb-6 uppercase text-xs tracking-widest text-white/40"
            >
              Navigation
            </h2>
            <ul class="flex flex-col gap-4">
              <li v-for="link in navLinks" :key="link.name">
                <NuxtLink
                  :to="link.to"
                  class="text-white/70 hover:text-green-400 transition-colors"
                >
                  {{ link.name }}
                </NuxtLink>
              </li>
            </ul>
          </nav>

          <nav>
            <h2
              class="font-bold mb-6 uppercase text-xs tracking-widest text-white/40"
            >
              Réseaux
            </h2>
            <ul class="flex flex-col gap-4">
              <li v-for="social in socialLinks" :key="social.name">
                <NuxtLink
                  :to="social.to"
                  class="text-white/70 hover:text-green-400 transition-colors flex items-center gap-2"
                >
                  {{ social.name }}
                </NuxtLink>
              </li>
            </ul>
          </nav>
        </div>
      </div>

      <div class="h-px w-full bg-white/10"></div>

      <div
        class="flex flex-col md:flex-row justify-between items-center gap-4 py-8"
      >
        <span class="text-sm text-white/40">
          © {{ new Date().getFullYear() }} Maurice Mumbere. Tous droits
          réservés.
        </span>
        <div
          class="flex items-center gap-2 text-xs text-white/20 uppercase tracking-widest"
        >
          <span>Built with</span>
          <span class="text-white/50">Nuxt</span>
          <span>&</span>
          <span class="text-white/50">Tailwind CSS</span>
        </div>
      </div>
    </div>
  </footer>
</template>
