<template>
    <section class="page min-h-screen" data-theme="light">
        <header>
            <Header />
        </header>
        <main class="mx-auto max-w-6xl min-h-screen px-3 2xl:px-0">
            <Messages />
            <Breadcrumb />
            <CookieBanner />
            <BackToTop />
            <slot />
        </main>
        <footer>
            <Footer />
        </footer>
    </section>
</template>
<script setup lang="ts">
import "../main.css";
import Footer from "~/components/Footer.vue";
import Header from "~/components/Header.vue";
</script>

<style scoped>
.page {
  --s: 100px; /* control the size*/
  --c1: #eceddc;
  --c2: #29ab87;
  
  --_g: var(--c1) 90deg,#0000 90.5deg;
  background:
   conic-gradient(from -45deg,var(--_g)),
   conic-gradient(from 135deg,var(--_g)) calc(var(--s)/2) 0,
   var(--c2);
  background-size: var(--s) var(--s)
}
</style>

