---
layout: post
codemirror: true
title: Debugging & Documentation (Ocean Adventure)
description: This explains how we used debugging tools, comments, and documentation while building Ocean Adventure.
permalink: /debugging-documentation
---

### Code Comments

Code comments helped us explain what different parts of our Ocean Adventure code were doing. Since our game had lots of enemies, coins, movement systems, and scoring logic, comments made the code easier to understand and fix later.

We used comments for:

- explaining enemy movement logic  
- labeling collision systems  
- organizing game objects  
- describing scoring features  

<div class="code-runner">
<pre><code class="language-javascript">
// Shark enemy follows the closest player

const speed = 2.2;

// Move shark toward player
this.position.x += Math.cos(angle) * speed;
</code></pre>
</div>

---

### Mini-Lesson Documentation

Mini-lesson documentation helped explain how different game systems worked. We wrote step-by-step explanations so other people could understand our Ocean Adventure project.

We used documentation for:

- explaining update() functions  
- teaching collision detection  
- showing how enemies follow players  
- describing scoring systems  

<div class="code-runner">
<pre><code class="language-javascript">
// Example mini-lesson explanation

/*
This update function runs every frame.
It checks the distance between the shark
and the player so the shark can chase them.
*/
</code></pre>
</div>

---

### Code Highlights

Code highlights made important parts of our code easier to notice and understand. This helped when debugging or teaching game systems.

We highlighted code for:

- collision detection  
- enemy movement  
- player controls  
- scoring systems  

<div class="code-runner">
<pre><code class="language-javascript">
// Important collision check

if (dist < 40) {
    console.log("Player hit!");
}
</code></pre>
</div>

---

### Console Debugging

Console debugging helped us test and fix problems in the game by printing information into the console.

We used console debugging for:

- checking player positions  
- testing enemy movement  
- tracking score updates  
- finding collision bugs  

<div class="code-runner">
<pre><code class="language-javascript">
// Console debugging example

console.log("Player X Position:", player.position.x);

console.log("Current Score:", score);
</code></pre>
</div>

---

### Hit Box Visualization

Hit box visualization helped us see the invisible collision areas around players, sharks, and objects. This made it easier to fix collision problems.

We used hit boxes for:

- enemy collisions  
- wall collisions  
- coin collection  
- player interactions  

<div class="code-runner">
<pre><code class="language-javascript">
// Hitbox example

const hitbox = {
    widthPercentage: 0.4,
    heightPercentage: 0.4
};

console.log(hitbox);
</code></pre>
</div>

---

### Source-Level Debugging

Source-level debugging helped us go through the code line by line to figure out exactly where problems were happening.

We used source-level debugging for:

- fixing update() errors  
- checking collision logic  
- testing player movement  
- debugging enemy AI  

<div class="code-runner">
<pre><code class="language-javascript">
// Source-level debugging example

function movePlayer() {

    debugger;

    console.log("Moving player...");
}

movePlayer();
</code></pre>
</div>

---

### Network Debugging

Network debugging helped us check if outside data and resources were loading correctly.

We used network debugging for:

- loading images and sprites  
- checking leaderboard requests  
- verifying API calls  
- testing game assets  

<div class="code-runner">
<pre><code class="language-javascript">
// Network request example

fetch("https://example.com/leaderboard")
    .then(response => response.json())
    .then(data => {
        console.log(data);
    });
</code></pre>
</div>

---

### Application Debugging

Application debugging helped us test the whole game and make sure different systems worked together correctly.

We used application debugging for:

- checking score systems  
- testing level loading  
- fixing enemy movement bugs  
- making sure cooldown systems worked  

<div class="code-runner">
<pre><code class="language-javascript">
// Application debugging example

if (gameOver) {
    console.log("Game has ended");
} else {
    console.log("Game still running");
}
</code></pre>
</div>

---

### Element Inspection

Element inspection helped us view and edit parts of the game directly in the browser. This was useful for testing visuals and UI elements.

We used element inspection for:

- checking scoreboards  
- testing canvas elements  
- fixing positioning issues  
- adjusting game UI  

<div class="code-runner">
<pre><code class="language-javascript">
// Element inspection example

const scoreboard = document.getElementById("game-scoreboard");

console.log(scoreboard);
</code></pre>
</div>

---

### Summary

Debugging and documentation were super important while building Ocean Adventure. Comments and mini-lessons helped explain the code, while debugging tools helped us find and fix problems faster.

Without debugging systems, it would have been really hard to build enemy movement, collisions, scoring, and all the other game features correctly.