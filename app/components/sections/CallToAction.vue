<template>
  <section class="max-w-6xl mx-auto px-6 py-20">
    <div
      class="bg-gray-50 rounded-[3rem] p-8 md:p-20 text-center border border-gray-100 shadow-sm"
    >
      <h2
        class="font-bold text-4xl md:text-6xl text-gray-900 max-w-2xl mx-auto leading-tight"
      >
        Prêt à faire décoller votre
        <span class="text-green-500">activité ?</span>
      </h2>

      <p class="max-w-md mx-auto py-8 text-gray-600 text-lg">
        Vous avez un projet de site, une refonte ou une interface à concevoir ?
        Parlons-en ensemble, je serais ravi de vous accompagner.
      </p>

      <NuxtLink
        to="https://wa.me/243895703947"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex justify-center items-center gap-3 bg-black text-white px-10 py-5 rounded-full text-xl md:text-2xl shadow-2xl transition-all hover:bg-gray-800 hover:scale-105 active:scale-95 group"
        aria-label="Discuter sur WhatsApp"
      >
        <IconWhatsapp
          class="w-8 h-8 transition-transform group-hover:rotate-12"
        />
        <span class="font-bold">On en discute ?</span>
      </NuxtLink>

      <div
        class="mt-8 flex justify-center items-center gap-2 text-sm text-gray-400"
      >
        <span class="flex h-2 w-2 rounded-full bg-green-400"></span>
        Disponible pour de nouveaux projets
      </div>
    </div>
  </section>
</template>
