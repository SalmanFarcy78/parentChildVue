<template>
       <h3 class="text-blue-700 text-xl font-bold my-5">This Is Child Component</h3>
       <p class="my-5">
         {{ modelValue }}
      </p>
      <button class="bg-blue-500 text-white font-bold py-2 px-2 w-30" @click="$emit('update:modelValue', msgEmit())">
         Child Button
       </button>
</template>

<script setup>
 const propsValue  = defineProps(['modelValue'])
 defineEmits(['update:modelValue'])

 function msgEmit(){
     return 'HI THERE! THIS MESSAGE FROM CHILD';  
 }
</script>
