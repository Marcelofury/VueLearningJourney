<template>
  <main class="app-wrapper">
    <header class="main-header">
      <h1>My Coursera Vue.js Learning Journey</h1>
      <p>Tracking daily progress and pushing modules to Github Chronologically</p>
      
    </header>
    <Part1_CreateComponents />
    <Part2_Interpolation />
  </main>
</template>

<script setup>

// step 1: Import the component using its exact file path

import Part1_CreateComponents from './components/Part1_CreateComponents.vue'
import Part2_Interpolation from './components/Part2_Interpolation.vue'

</script>

<style>
/** Notice there is NO 'scoped' here.
These are global styles that format our overall page layout.
 */

body{
  background-color: #eef2f5;
  margin:0;
  padding: 0;
}

.app_wrapper{
  padding: 40px 20px;
}

.main-header{
  text-align: center;
  margin-bottom: 40px;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.main-header{
  color: #35495e;
}

</style>