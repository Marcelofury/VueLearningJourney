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