<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const person = {
  name: 'Hasan Ali',
  title: 'Web Developer',
  url: 'https://i.ibb.co/zrZy1np/profile-resizer.jpg'
}

const messageToChild = 'Hello from Parent';
const messageFromChild = ref('');

</script>


<template>
  <div class="p-12 bg-slate-100">
    <p class="mt-4 font-semibold text-2xl">Photo show from child:</p>
    <div class="avatar my-5">
      <div class="w-32 rounded-full shadow-lg border-2">
        <img :src="messageFromChild ? messageFromChild : 'https://brur.ac.bd/wp-content/uploads/2019/03/male.jpg'" />
      </div>
    </div>
    
    <ChildComponent :person="person" :messageToChild="messageToChild"  v-model:messageFromChild="messageFromChild" />
  </div>
</template>


<style scoped>
/* Add Tailwind CSS classes here if needed */
</style>
