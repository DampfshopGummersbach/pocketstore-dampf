<template>
  <div class="px-3 mx-auto max-w-6xl mb-3">
    <section
      class="bg-black rounded-xl mx-auto max-w-6xl px-3 py-3 text-white flex justify-between items-end"
    >
      <section class="logo h-16 flex items-center ml-6">Gummersbach-Dampfer.shop</section>
      <nav class="desktop">
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
    </section>
  </div>
</template>

<script setup lang="ts">
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { faSmoking } from "@fortawesome/free-solid-svg-icons";
</script>