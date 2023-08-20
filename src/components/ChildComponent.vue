<script setup>
import { defineProps } from 'vue';

defineProps(['person', 'messageToChild', 'messageFromChild'])
defineEmits(['update:messageFromChild'])
</script>

<template>
  <div class="border-2 p-10">
      <div>
        <h1 class="text-2xl font-semibold mb-3">{{ messageToChild }}</h1>
      </div>

      <div>
        <!-- <img class="w-32 h-32 rounded-lg" :src="person.url" alt=""> -->
        <div>
          <h1 class="text-xl font-medium">{{ person.name }}</h1>
          <h1 class="text-xl font-medium">{{ person.title }}</h1>
        </div>
        <div class="flex gap-2 my-5">
          <button @click="$emit('update:messageFromChild', person.url)" class="bg-blue-500 text-white focus:outline-none">Show</button>
          <button @click="$emit('update:messageFromChild', '')" class="bg-blue-500 text-white focus:outline-none">Hide</button>
        </div>
      </div>
  </div>
</template>
  