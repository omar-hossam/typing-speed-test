<script setup>
import Logo from "@images/logo-small.svg"
import Trophy from "@images/icon-personal-best.svg"
import { ref } from 'vue'

const score = ref(92)
  
</script>
<template>
  <header>
    <nav>
      <ul class="flex justify-between items-center">
	<li class="flex gap-2 select-none">
	  <div>
	    <img :src="Logo" alt="keyboard image" class="w-12 h-full object-center object-cover" />
	  </div>
	  <div>
	    <h1 class="font-bold text-3xl pb-[2px]">Typing Speed Test</h1>
	    <p class="text-sm text-slate-700">Type as fast as you can in 60 seconds</p>
	  </div>
	</li>
	
	<li class="flex items-center gap-2">
	  <div>
	    <img :src="Trophy" />
	  </div>
	  <p class="text-slate-700">Personal best: <strong class="text-black">{{ score }}</strong></p>
	</li>
      </ul>
    </nav>
  </header>
</template>
