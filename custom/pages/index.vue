<template>
  <section class="page">
    <div class="mx-auto max-w-6xl grid grid-cols-6 gap-3">
      <div class="col-span-6">
        <section
          class="bg-gradient-to-r from-sky-700 to-indigo-800 text-white rounded-xl"
        >
          <div
            class="max-w-7xl mx-auto px-12 py-20 flex flex-col md:flex-row items-center gap-8"
          >
            <!-- Text -->
            <div class="flex-1">
              <h1 class="text-4xl md:text-6xl font-bold mb-4">
                Wolken. Geschmack. Freiheit.
              </h1>
              <p class="text-lg mb-6">
                Entdecke die neuesten E-Zigaretten, Liquids und Zubehör für dein
                perfektes Dampferlebnis.
              </p>
              <div class="space-x-4">
                <button class="btn btn-primary">Jetzt einloggen</button>
                <button class="btn btn-outline btn-neutral">
                  {{ $t('catalog.cta.to-products') }}
                </button>
              </div>
            </div>

            <!-- Bild -->
            <div class="flex-1 relative">
              <img
                src="/unsplash/e-liquids-uk-hVcmxpYg1Gc-unsplash.jpg"
                alt="Vape"
                class="rounded-2xl shadow-2xl mx-auto md:mx-0"
              />
            </div>
          </div>
        </section>
      </div>
      <CatalogProductGrid identifier="dampfer" />
      <CatalogProductGrid identifier="vapes" />
    </div>
  </section>
</template>

<script setup lang="ts">
const { t } = useI18n();
useHead({
  title: t("general.title"),
  meta: [
    {
      name: "description",
      content:
        "PocketStore.io is a Open Source Shop Framework which is based on PocketBase and made with Nuxt/VueJs by Jonathan Martz.",
    },
  ],
});
</script>