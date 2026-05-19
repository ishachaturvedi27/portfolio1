---
layout: post
codemirror: true
title: Advanced Game Features & Data Handling (Ocean Adventure)
description: This explains how we used operators, rendering, APIs, and data systems in our Ocean Adventure game.
permalink: /advanced-features
---

### Mathematical Operators

Mathematical operators were super important in Ocean Adventure because they controlled movement, scoring, collisions, and distances between objects.

We used math operators for:

- adding points when coins were collected  
- calculating enemy movement  
- checking collision distance  
- controlling player and shark speed  

<div class="code-runner">
<pre><code class="language-javascript">
// Mathematical operators in Ocean Adventure

let score = 0;

score += 10;

let dx = 50 - 20;
let dy = 80 - 40;

let distance = Math.sqrt(dx * dx + dy * dy);

console.log(distance);
</code></pre>
</div>

---

### String Operations

String operations helped display text and messages throughout the game. They made the game feel more interactive and easier to understand.

We used string operations for:

- NPC dialogue  
- score messages  
- game over text  
- player and enemy names  

<div class="code-runner">
<pre><code class="language-javascript">
// String operations example

let playerName = "Octopus";
let message = playerName + " collected a coin!";

console.log(message);
</code></pre>
</div>

---

### Boolean Expressions

Boolean expressions checked whether something was true or false. These were constantly used during gameplay.

We used booleans for:

- collision checks  
- cooldown systems  
- checking if the player was alive  
- controlling game over states  

<div class="code-runner">
<pre><code class="language-javascript">
// Boolean expression example

let touchingEnemy = true;
let cooldownActive = false;

if (touchingEnemy && !cooldownActive) {
    console.log("Player takes damage!");
}
</code></pre>
</div>

---

### Keyboard Input

Keyboard input allowed the player to actually control the octopus in Ocean Adventure.

We used keyboard input for:

- WASD movement  
- controlling direction  
- interacting with objects  
- moving through levels  

<div class="code-runner">
<pre><code class="language-javascript">
// Keyboard input example

document.addEventListener("keydown", function(event) {

    if (event.key === "w") {
        console.log("Move Up");
    }

    if (event.key === "a") {
        console.log("Move Left");
    }

});
</code></pre>
</div>

---

### Canvas Rendering

Canvas rendering helped draw the game objects onto the screen. This is what actually made the player, sharks, and backgrounds visible during gameplay.

We used canvas rendering for:

- drawing the ocean background  
- displaying sharks and coins  
- showing movement animations  
- updating objects every frame  

<div class="code-runner">
<pre><code class="language-javascript">
// Canvas rendering example

const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");

ctx.fillStyle = "blue";
ctx.fillRect(50, 50, 100, 100);
</code></pre>
</div>

---

### GameEnv Configuration

GameEnv configuration helped control the setup of the game environment. This made it easier to organize levels, dimensions, and game objects.

We used GameEnv configuration for:

- setting screen width and height  
- loading levels  
- storing game objects  
- controlling game settings  

<div class="code-runner">
<pre><code class="language-javascript">
// GameEnv configuration example

const gameEnv = {
    width: 800,
    height: 600,
    score: 0
};

console.log(gameEnv.width);
</code></pre>
</div>

---

### API Integration

API integration allowed our game to connect with outside systems and load or save information.

We used API concepts for:

- leaderboard systems  
- saving scores  
- loading game information  
- connecting data between systems  

<div class="code-runner">
<pre><code class="language-javascript">
// API fetch example

fetch("https://example.com/leaderboard")
    .then(response => response.json())
    .then(data => {
        console.log(data);
    });
</code></pre>
</div>

---

### Asynchronous I/O

Asynchronous I/O allowed parts of the game to load without freezing everything else. This helped the game stay smooth while loading data.

We used asynchronous systems for:

- loading leaderboard data  
- fetching outside information  
- handling timers and cooldowns  
- loading assets in the background  

<div class="code-runner">
<pre><code class="language-javascript">
// Async function example

async function loadLeaderboard() {

    let response = await fetch("https://example.com/data");
    let data = await response.json();

    console.log(data);
}

loadLeaderboard();
</code></pre>
</div>

---

### JSON Parsing

JSON parsing helped organize and read game data in a structured way. This made storing information much cleaner.

We used JSON parsing for:

- player settings  
- leaderboard information  
- enemy data  
- game configuration  

<div class="code-runner">
<pre><code class="language-javascript">
// JSON parsing example

let sharkData = '{"name":"Shark","damage":10}';

let parsedData = JSON.parse(sharkData);

console.log(parsedData.name);
</code></pre>
</div>

---

### Summary

All of these advanced programming concepts helped make Ocean Adventure feel like a real game. Mathematical operators controlled movement and scoring, rendering displayed objects on the screen, APIs handled outside data, and JSON kept everything organized.

Without these systems, the game would not feel smooth, interactive, or complete.