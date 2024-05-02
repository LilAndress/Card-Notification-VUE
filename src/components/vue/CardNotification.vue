<script setup>
import { ref } from "vue";
 const counter = ref(0)

 function decrement() {
    if (counter.value > 0) {
    
    counter.value--
    }
    
 }

 function increment(){
 counter.value++

 }
</script>


<template>

 <div class=" flex-col bg-slate-200 rounded py-8 px-6 w-96 flex items-center shadow-md">
	<div class="relative">
		<img class="size-32 rounded-full" src="https://i.ytimg.com/vi/VW3BlnAainM/maxresdefault.jpg">
    
	  <div v-show="counter > 0" class=" absolute top-0 right-0 size-6 rounded-full bg-red-500 text-white flex justify-center items-center">
        {{ counter }}
	   </div>
       
	 </div>
     <p v-if="counter > 0">Tienes mensajes nuevos! 😈 </p>
       <p  v-else= ""> Nadie te habla 😿</p>

	 <div class="flex justify-around w-24 mt-6">
		<button @click="decrement" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">-</button>
		 {{ counter }}
		<button  @click="increment" class="bg-blue-200 rounded w-6 flex justify-center items-center px-2">+</button>
     	</div>
	  </div>

</template>