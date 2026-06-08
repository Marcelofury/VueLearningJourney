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