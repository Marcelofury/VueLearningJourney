<template>
  <div class="component-card">
    
    <h2>Part 1: Creating a Basic Component</h2>
    <p>
      Congratulations! You have successfully created, exported, and imported 
      your very first custom Vue component.
    </p>

    <div class="status-badge">
      Status: Active & Rendered
    </div>

  </div>
</template>

<script setup>
/* Why '<script setup>'?
  - This is Vue 3's modern syntax. 
  - Any variable or import declared here is automatically available to the <template> above.
  - You don't need boilerplate code like `export default` or `data() {}`.
*/

// For this absolute basic component, no complex JavaScript logic is needed yet!
console.log("Part1_CreateComponents has successfully mounted to the DOM!")
</script>

<style scoped>
/* The 'scoped' attribute ensures that these styles ONLY apply to this component. 
  It will not accidentally change styles anywhere else in your app.
*/
.component-card {
  border: 2px solid #42b883; /* Distinctive Vue Green color */
  border-radius: 12px;
  padding: 24px;
  margin: 15px auto;
  max-width: 600px;
  background-color: #f8f9fa;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
  font-family: Arial, sans-serif;
}

h2 {
  color: #35495e; /* Sleek Vue Dark Charcoal */
  margin-top: 0;
}

p {
  color: #555;
  line-height: 1.6;
}

.status-badge {
  display: inline-block;
  background-color: #42b883;
  color: white;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: bold;
}
</style>