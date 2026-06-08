<template>
    <div class="component-card methods-theme" >
        <h2>Part 3 : Methods and Parameters</h2>
        <p> Methods are functions that run in response to user actios.We use the <strong>v-on:</strong> directive (or its shorthand <strong>@</strong>) to listen for events</p>
    </div>

    <div class="demo-box">
        <h3>1. Basic Method (No Parameters)</h3>
        <p>Videos Reviewed : <mark> {{ videoCount }}</mark></p>

        <button class="btn" @click="incrementVideos" >+1 Video Completed</button>
    </div>

    <div class="demo-box">
        <h3>2, Method with Custom Parameters</h3>
        <p>Click a topic to instantly log its stimated study length via a method parameter:</p>

        <div class="button-group">
            <button class="btn-secondary" @click="logTopicDetails('Methods & Parameters',5)"> Check Topic A</button>
            <button class="btn-secondary" @click="logTopicDetails('Events & Parameters', 4)"> Check Topic B</button>
        </div>
        <p v-if="feedbackMessage" class="feedback-text">
            Status: <span>{{ feedbackMessage }}</span>
        </p>
    </div>
</template>

<script>
import {ref} from 'vue'

// Reactive state tracking our data variables
const videoCount = ref(2) // simulatinf that we have completed 2 video items so far

const feedbackMessage = ref('')

// METHOS (standard Javascript functions)

/**
 * Method 1: Basic function without parameters.
 * Remember: Inside the <script setup> block, we must use '.value' to access or mutate a variable declared with ref().
 */
const incrementVideo = ()=>{
    videoCount.value++
    console.log(`Video Count updated to : ${videoCount.value}`)
}

/**
 * Method 2; Function that accepts parameters.
 * This takes 'topicName' and 'duration' from the template template button action and processes them dynamically
 */

const logTopicDetails =(topicName, duration) => {
    feedbackMessage.value = `Targeting "${topicName}" which requires ${duration} minnutes.`
    console.log(`User inspected topic: ${topicName} (${duration} mins)`)
}
</script>

<style scoped>
.methods-theme {
border: 2px solid #42b883;
background-color: #ffffff;
border-radius: 12px;
padding: 24px;
margin: 20px auto;
max-width: 600px;
box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
font-family: Arial, Helvetica, sans-serif;
}
h2{
    color: #35495e;
    margin-top: 0;
}


</style>