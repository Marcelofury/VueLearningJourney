<template>
    <div class="component-card interpolation-theme">

        <h2> Part2: Vue.js Interpolation</h2>
        <p> Interpolation allows us to bind reactive text variables dynamically.If the data changes in the script, the view below updates instantly</p>

        <div class="demo-box">
            <h3> Student Profile</h3>
            <p><strong>Name:</strong> {{ studentName }}</p>
            <p><strong>Learning Platform:</strong> {{ platform }}</p>
            <p><strong>Module progress:</strong>{{ currentModule }} out of {{ totalModules }}</p>

            <p><strong>Modules Remaining</strong>{{ totalModules - currentModule }}</p>

            <p><strong>Status Check</strong> {{ currentModule === totalModules ? 'Completed' : 'Work in progress'}}</p>
        </div>
    </div>
</template>

<script setup>
/**To make data 'reactive'(meaning Vue watches it and updates the screen when it changes), we must import 'ref' from the the core 'vue' package.
 * 
 * 
 * 
 */

 import ref from 'vue'

 //Declaring reactive string data types

 const studentName = ref('Software Developer')
 const platform = ref('Coursera')

 //Declaring reactive number data types

 const currentModule = ref(2)
 const totalModules = ref(10)

 /*  NOTE FOR GITHUB DOCUMENTATION:
  When using <script setup>, any variable declared here with `ref()` 
  can be used directly in the <template> by its name (e.g., studentName).
  However, if you want to read or change its value inside this script block, 
  you must append `.value` (e.g., currentModule.value = 3).
*/
console.log(`Currently testing interpolation for module: ${currentModule.value}`)

</script>

<style scoped>
/** Scoped styles ensure this distinct theme doesn't bleed into Part 1

*/
.interpolation-theme{
    border: 2px solid #35495e;
    background-color: #ffffff;
    border-radius: 12px;
    padding: 24px;
    margin: 20px auto;
    max-width: 600px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    font-family: Arial, sans-serif;
}
h2{
    color: #35495e;
    margin-top: 0;
}

.demo-box{
    background-color: #f1f5f9;
    border-left: 4px solid #35495e;
    padding:15px;
    border-radius: 4px;
    margin-top: 15px;
}

</style>