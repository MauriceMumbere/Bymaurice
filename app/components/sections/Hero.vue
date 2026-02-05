<template>
  <section
    class="min-h-[90vh] flex justify-center items-center px-6 py-20 bg-white"
    id="home"
  >
    <div class="max-w-4xl mx-auto text-center">
      <div class="relative flex justify-center pb-10">
        <div
          class="absolute inset-0 m-auto w-32 h-32 bg-green-100 rounded-full blur-2xl opacity-50"
        ></div>
        <img
          class="relative h-48 w-48 object-cover rounded-full border-4 border-white shadow-xl"
          src="/images/profile.png"
          alt="Portrait de [Ton Nom]"
        />
      </div>

      <div>
        <h1
          class="text-4xl md:text-6xl font-extrabold tracking-tight text-gray-900 leading-tight"
        >
          Créons ensemble votre <br />
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-green-500 to-black"
          >
            vitrine digitale.
          </span>
        </h1>
      </div>

      <p
        class="mt-8 text-lg md:text-xl text-gray-600 max-w-xl mx-auto leading-relaxed"
      >
        De l’idée au produit final : design, développement et mise en ligne.
        Expert en solutions Web et Mobile.
      </p>

      <div
        class="mt-10 flex flex-col sm:flex-row justify-center items-center gap-4"
      >
        <NuxtLink
          to="https://wa.me/33612345678"
          target="_blank"
          class="w-full sm:w-auto flex items-center justify-center gap-2 bg-black text-white px-8 py-4 rounded-full font-bold shadow-xl transition-all hover:bg-gray-800 hover:scale-105 active:scale-95"
        >
          <IconWhatsapp class="w-6 h-6" />
          Discutons de votre projet
        </NuxtLink>

        <NuxtLink
          to="#about"
          class="w-full sm:w-auto px-8 py-4 rounded-full font-bold border-2 border-gray-100 text-gray-900 hover:bg-gray-50 transition-all active:scale-95"
        >
          Me découvrir
        </NuxtLink>
      </div>
    </div>
  </section>
</template>
