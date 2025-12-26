<script setup>
import Logo from "@images/logo-small.svg"
import Trophy from "@images/icon-personal-best.svg"
import { ref } from 'vue'

const score = ref(92)
  
</script>
<template>
  <header>
    <nav>
      <ul>
	<li>
	  <a href="/">
	    <div>
	      <img :src="Logo" />
	    </div>
	    <div>
	      <h1>Typing Speed Test</h1>
	      <p>Type as fast as you can in 60 seconds</p>
	    </div>
	  </a>
	</li>
	
	<li>
	  <div>
	    <img :src="Trophy" />
	  </div>
	  <p>Personal best: <strong>{{ score }}</strong></p>
	</li>
      </ul>
    </nav>
  </header>
</template>
