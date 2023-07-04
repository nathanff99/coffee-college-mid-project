<template>
  <div id="app">
    <Navbar />

    <main>
      <Banner />
      <About />
      <Trending />
      <Delivery />
      <Contact />
    </main>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from "./components/core/Navbar.vue";
import Banner from "./components/home/Banner.vue";
import About from "./components/home/About.vue";
import Trending from "./components/home/Trending.vue";
import Delivery from "./components/home/Delivery.vue";
import Contact from "./components/home/Contact.vue";
import Footer from "./components/core/Footer.vue";
</script>