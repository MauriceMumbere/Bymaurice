<script setup>
import IconVue from "~/components/icons/IconVue.vue";
import IconNuxt from "~/components/icons/IconNuxt.vue";
import IconNodeJs from "~/components/icons/IconNodeJs.vue";
import IconTailwindCss from "~/components/icons/IconTailwindCss.vue";
import IconSupaBase from "~/components/icons/IconSupaBase.vue";
import IconWordPress from "~/components/icons/IconWordPress.vue";

const tools = [
  { name: "Vue.js", component: IconVue },
  { name: "Nuxt", component: IconNuxt },
  { name: "Node.js", component: IconNodeJs },
  { name: "Tailwind", component: IconTailwindCss },
  { name: "Supabase", component: IconSupaBase },
  { name: "WordPress", component: IconWordPress },
];
</script>
<template>
  <section class="max-w-6xl mx-auto px-6 py-20" id="about">
    <div class="text-center mb-16">
      <div
        class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-green-50 text-green-600 font-medium text-sm mb-4"
      >
        <span class="h-2 w-2 rounded-full bg-green-400 animate-pulse"></span>
        À propos
      </div>
      <h2 class="font-bold text-4xl md:text-5xl text-gray-900">
        Un peu plus sur moi
      </h2>
    </div>

    <div class="bg-gray-50 p-4 rounded-3xl border border-gray-100">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div
          class="bg-white rounded-2xl p-8 shadow-sm flex flex-col justify-center"
        >
          <h3 class="text-2xl font-bold mb-4 text-gray-800">Mon profil</h3>
          <div class="space-y-4 text-gray-600 leading-relaxed">
            <p>
              Développeur web et mobile passionné par la création d'applications
              modernes. Formé à la
              <span class="text-black font-semibold">Kadea Academy</span>, je
              maîtrise l'ensemble de la chaîne de production, du backend au
              frontend.
            </p>
            <p>
              Curieux et rigoureux, je transforme vos idées en solutions
              performantes et intuitives, en restant toujours à l'affût des
              dernières innovations technologiques.
            </p>
          </div>
        </div>

        <div class="h-full">
          <img
            class="rounded-2xl w-full h-full max-h-[450px] object-cover shadow-sm"
            src="/images/about_image.jpeg"
            alt="Portrait de développeur"
          />
        </div>

        <div class="bg-white rounded-2xl p-8 shadow-sm md:col-span-2">
          <h3
            class="pb-6 font-bold text-xl text-gray-800 text-center md:text-left"
          >
            Mes outils favoris
          </h3>
          <div class="flex flex-wrap justify-center md:justify-between gap-6">
            <div
              v-for="(icon, index) in tools"
              :key="index"
              class="group flex flex-col items-center gap-2"
            >
              <div
                class="bg-gray-50 p-4 rounded-xl transition-all duration-300 group-hover:bg-black group-hover:text-white group-hover:-translate-y-1 shadow-sm"
              >
                <component :is="icon.component" class="w-8 h-8" />
              </div>
              <span class="text-xs font-medium text-gray-500">{{
                icon.name
              }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
