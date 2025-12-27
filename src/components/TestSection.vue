<script setup>
  import { ref } from "vue"
  
  const text = ref("The archaeological expedition unearthed artifacts that complicated prevailing theories about Bronze Age trade networks. Obsidian from Anatolia, lapis lazuli from Afghanistan, and amber from the Baltic—all discovered in a single Mycenaean tomb—suggested commercial connections far more extensive than previously hypothesized. \"We've underestimated ancient peoples' navigational capabilities and their appetite for luxury goods,\" the lead researcher observed. \"Globalization isn't as modern as we assume.\"")
</script>
<template>
  <section class="w-full py-2">
    <div class="w-full h-full md:text-2xl/10 xl:text-3xl/12 py-3 text-gray-400 outline-0 resize-none" aria-label="Type to start the test">
      {{ text }}
    </div>
  </section>
</template>
