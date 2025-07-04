<template>
  <div class="px-3 xl:px-0 mx-auto max-w-6xl mb-3">
    <section
      class="bg-black rounded-xl mx-auto max-w-6xl px-3 py-3 text-white flex justify-between items-end"
    >
      <section class="logo text-2xl flex items-center">
        Gummersbach-Dampfer.shop
      </section>
      <nav class="desktop hidden md:flex">
        <ul class="flex space-x-6">
          <li>
            <a href="/">
              <FontAwesomeIcon :icon="faSmoking" />
              <span class="ml-3">Hallo Welt</span>
            </a>
          </li>
          <li>
            <a href="/">
              <FontAwesomeIcon :icon="faSmoking" />
              <span class="ml-3">Hallo Welt</span>
            </a>
          </li>
          <li>
            <a href="/">
              <FontAwesomeIcon :icon="faSmoking" />
              <span class="ml-3">Hallo Welt</span>
            </a>
          </li>
          <li>
            <a href="/">
              <FontAwesomeIcon :icon="faSmoking" />
              <span class="ml-3">Hallo Welt</span>
            </a>
          </li>
        </ul>
      </nav>
      <nav class="mobile md:hidden flex items-center">
        <div v-if="!open" class="bars">
          <button @click.prevent="open = !open">
            <FontAwesomeIcon color="white" size="2x" :icon="faBars" />
          </button>
        </div>
        <div v-else class="times">
          <button @click.prevent="open = !open">
            <FontAwesomeIcon color="white" size="2x" :icon="faTimes" />
          </button>
        </div>
      </nav>
    </section>
    <section v-if="open" class="mobile-content my-2">
      <section class="grid grid-cols-6 gap-3 bg-gray-400 px-3 py-3">
        <div
          v-for="category in categories"
          :key="category.id"
          class="col-span-2"
        >
          <a :href="'/de/category/'+category.slug+'.html'" class="btn btn-neutral btn-sm btn-block">{{
            category.name
          }}</a>
        </div>
      </section>
    </section>
  </div>
</template>

<script setup lang="ts">
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faSmoking, faBars, faTimes } from "@fortawesome/free-solid-svg-icons";
import { useLocalStorage } from "@vueuse/core";
import { usePocketBase } from "~/util/pocketbase";

const open = useLocalStorage("open-navigation", false, {});
const categories = ref([]);
const pb = usePocketBase();

const load = async () => {
  categories.value = (await pb.collection("categories").getList(1,10)).items;
};

onMounted(() => {
  load();
});
</script>