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

{% capture challenge_cs111_demo_1 %}
Mathematical Operators
{% endcapture %}

{% capture code_cs111_demo_1 %}
let score = 0;

score += 10;

let dx = 50 - 20;
let dy = 80 - 40;

let distance = Math.sqrt(dx * dx + dy * dy);

console.log(distance);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-1"
   language="javascript"
   challenge=challenge_cs111_demo_1
   code=code_cs111_demo_1
%}

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

{% capture challenge_cs111_demo_2 %}
String Operations
{% endcapture %}

{% capture code_cs111_demo_2 %}
let playerName = "Octopus";
let message = playerName + " collected a coin!";

console.log(message);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-2"
   language="javascript"
   challenge=challenge_cs111_demo_2
   code=code_cs111_demo_2
%}

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

{% capture challenge_cs111_demo_3 %}
Boolean Expressions
{% endcapture %}

{% capture code_cs111_demo_3 %}
let touchingEnemy = true;
let cooldownActive = false;

if (touchingEnemy && !cooldownActive) {
    console.log("Player takes damage!");
}
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-3"
   language="javascript"
   challenge=challenge_cs111_demo_3
   code=code_cs111_demo_3
%}

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

{% capture challenge_cs111_demo_4 %}
Keyboard Input
{% endcapture %}

{% capture code_cs111_demo_4 %}
document.addEventListener("keydown", function(event) {

    if (event.key === "w") {
        console.log("Move Up");
    }

    if (event.key === "a") {
        console.log("Move Left");
    }

});
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-4"
   language="javascript"
   challenge=challenge_cs111_demo_4
   code=code_cs111_demo_4
%}

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

{% capture challenge_cs111_demo_5 %}
Canvas Rendering
{% endcapture %}

{% capture code_cs111_demo_5 %}
const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");

ctx.fillStyle = "blue";
ctx.fillRect(50, 50, 100, 100);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-5"
   language="javascript"
   challenge=challenge_cs111_demo_5
   code=code_cs111_demo_5
%}

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

{% capture challenge_cs111_demo_6 %}
GameEnv Configuration
{% endcapture %}

{% capture code_cs111_demo_6 %}
const gameEnv = {
    width: 800,
    height: 600,
    score: 0
};

console.log(gameEnv.width);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-6"
   language="javascript"
   challenge=challenge_cs111_demo_6
   code=code_cs111_demo_6
%}

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

{% capture challenge_cs111_demo_7 %}
API Integration
{% endcapture %}

{% capture code_cs111_demo_7 %}
fetch("https://example.com/leaderboard")
    .then(response => response.json())
    .then(data => {
        console.log(data);
    });
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-7"
   language="javascript"
   challenge=challenge_cs111_demo_7
   code=code_cs111_demo_7
%}

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

{% capture challenge_cs111_demo_8 %}
Asynchronous I/O
{% endcapture %}

{% capture code_cs111_demo_8 %}
async function loadLeaderboard() {

    let response = await fetch("https://example.com/data");
    let data = await response.json();

    console.log(data);
}

loadLeaderboard();
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-8"
   language="javascript"
   challenge=challenge_cs111_demo_8
   code=code_cs111_demo_8
%}

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

{% capture challenge_cs111_demo_9 %}
JSON Parsing
{% endcapture %}

{% capture code_cs111_demo_9 %}
let sharkData = '{"name":"Shark","damage":10}';

let parsedData = JSON.parse(sharkData);

console.log(parsedData.name);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-9"
   language="javascript"
   challenge=challenge_cs111_demo_9
   code=code_cs111_demo_9
%}

---

### Operators (General)

Operators in general are symbols that help the computer do actions with values. In Ocean Adventure, we used different types of operators all the time to make the game actually work.

We used operators for:

- doing math like adding scores and moving objects  
- comparing values like checking collisions or health  
- combining conditions using AND / OR logic  
- updating variables like speed and position  

<div class="code-runner">
<pre><code class="language-javascript">
// General operators example

let score = 10;

// arithmetic operator
score = score + 5;

// comparison operator
if (score >= 15) {
    console.log("Level up!");
}

// logical operator
let alive = true;
let hasPowerUp = false;

if (alive && !hasPowerUp) {
    console.log("Normal state");
}
</code></pre>
</div>

{% capture challenge_cs111_demo_10 %}
Operators (General)
{% endcapture %}

{% capture code_cs111_demo_10 %}
let score = 10;

// arithmetic operator
score = score + 5;

// comparison operator
if (score >= 15) {
    console.log("Level up!");
}

// logical operator
let alive = true;
let hasPowerUp = false;

if (alive && !hasPowerUp) {
    console.log("Normal state");
}
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-10"
   language="javascript"
   challenge=challenge_cs111_demo_10
   code=code_cs111_demo_10
%}

---

### Input / Output

Input and output is basically how the game talks to the player and how the player controls the game. Input is what the player does, and output is what the game shows back.

In Ocean Adventure, input and output were really important because they made the game interactive.

We used input/output for:

- keyboard controls (input from player)  
- showing movement and animations on screen (output)  
- displaying score updates and messages  
- reacting to player actions in real time  

<div class="code-runner">
<pre><code class="language-javascript">
// Input / Output example

document.addEventListener("keydown", function(event) {

    // INPUT (player presses a key)
    if (event.key === "w") {
        console.log("Player moves up");
    }

});

// OUTPUT (game shows result)
let score = 0;
score += 10;

console.log("Score is now " + score);
</code></pre>
</div>

{% capture challenge_cs111_demo_11 %}
Input / Output
{% endcapture %}

{% capture code_cs111_demo_11 %}
document.addEventListener("keydown", function(event) {

    // INPUT (player presses a key)
    if (event.key === "w") {
        console.log("Player moves up");
    }

});

// OUTPUT (game shows result)
let score = 0;
score += 10;

console.log("Score is now " + score);
{% endcapture %}

{% include runners/code.html
   runner_id="cs111-demo-11"
   language="javascript"
   challenge=challenge_cs111_demo_11
   code=code_cs111_demo_11
%}

---

### Summary

All of these advanced programming concepts helped make Ocean Adventure feel like a real game. Mathematical operators controlled movement and scoring, rendering displayed objects on the screen, APIs handled outside data, and JSON kept everything organized.

Without these systems, the game would not feel smooth, interactive, or complete.