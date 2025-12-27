<script setup>
  import Navbar from "@components/Navbar.vue";
  import Bar from "@components/Bar.vue";
  import TestSection from "@components/TestSection.vue";
  import RestartTestBtn from "@components/RestartTestBtn.vue";
</script>

<template>
  <Navbar />
  <main class="flex flex-col">
    <Bar />
    <hr class="border border-slate-200 rounded-lg" />
    <TestSection />
    <hr class="border border-slate-200 rounded-lg" />
    <RestartTestBtn />
  </main>
</template>

<style scoped></style>
