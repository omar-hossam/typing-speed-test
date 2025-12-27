<script setup>
  import { ref } from "vue";
  
  const wpm = ref(40)
  const accuracy = ref(94)
  const timeSeconds = ref(46)
  const difficulities = ref([
    {id: 1, name: 'Easy', chose: true},
    {id: 2, name: 'Medium', chose: false},
    {id: 3, name: 'Hard', chose: false}
  ])
  const modes = ref([
    {id: 1, name: 'Timed (60s)', chose: true},
    {id: 2, name: 'Passage', chose: false}
  ]) 
  
  function difficulityTrigger(difficulity) {
    difficulities.value.forEach(val => val.chose = val !== difficulity ? false : true)
  }
  function modeTrigger(mode) {
    modes.value.forEach(val => val.chose = val !== mode ? false : true)
  }	
</script>
<template>
  <section class="flex justify-between py-4">
    <!-- LEFT -->
    <div class="flex gap-4 xl:gap-5 2xl:gap-6 items-center">
      <!-- WPM -->
      <div class="flex gap-2 items-center">
	<span class="text-md text-slate-700">WPM: </span><strong class="text-xl">{{ 40 }}</strong>
      </div>
    
      <!-- ACCURACY -->
      <div class="flex gap-2 items-center">
	<span class="text-md text-slate-700">Accuracy: </span><strong class="text-xl text-green-600">{{ accuracy }}%</strong>
      </div>
      
      <!-- TIME -->
      <div class="flex gap-2 items-center">
	<span class="text-md text-slate-700">Time: </span><strong class="text-xl text-amber-600">{{ timeSeconds === 60 ? `1:00` : `0:${timeSeconds}` }}</strong>
      </div>
    
    </div>
    <!-- RIGHT -->
    <div class="flex gap-4">
      <!-- DIFFICULITY -->
      <div class="flex gap-1 items-center">
	<span class="text-md text-slate-700">Difficulity: </span>
	<ul class="flex gap-1">
	  <li v-for="difficulity in difficulities" :key='difficulity.id'>
	    <button class="cursor-pointer p-2 border-2 rounded-lg transition transition-100 ease-in-out" :class="difficulity.chose ? 'border-cyan-700 text-cyan-700' : 'border-slate-300'" @click="difficulityTrigger(difficulity)">{{ difficulity.name }}</button>
	  </li>
	</ul>
      </div>
      <!-- MODE -->
      <div class="flex gap-1 items-center">
	<span class="text-md text-slate-700">Mode: </span>
	<ul class="flex gap-1">
	  <li v-for="mode in modes" :key='mode.id'>
	    <button class="cursor-pointer p-2 border-2 rounded-lg transition transition-100 ease-in-out" :class="mode.chose ? 'border-cyan-700 text-cyan-700' : 'border-slate-300'" @click="modeTrigger(mode)">{{ mode.name }}</button>
	  </li>
	</ul>
      </div>
    </div>
  </section>
</template>
