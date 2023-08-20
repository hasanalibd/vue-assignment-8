<script>
import ParentComponent from './components/ParentComponent.vue';
export default {
  name: 'App',
  components: {
    ParentComponent,
  },
};
</script>

<template>
  <div class="min-h-screen flex items-center justify-center">
    <ParentComponent />
  </div>
</template>

<style>
/* Add Tailwind CSS classes here if needed */
</style>
