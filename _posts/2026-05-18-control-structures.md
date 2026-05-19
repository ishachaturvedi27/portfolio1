---
layout: post
codemirror: true
title: Control Structures & Data Types (Ocean Adventure)
description: This explains how we used control structures, loops, and data types to make Ocean Adventure work.
permalink: /control-structures
---

### Control Structures

Control structures helped our Ocean Adventure game decide what should happen while the game was running. Instead of everything happening at once, the game checks conditions and reacts to what the player does.

Here are some ways we used control structures in our game:

- checking if the octopus hit a shark or wall  
- controlling player movement with keyboard input  
- deciding when enemies should follow the player  
- handling level progression and game events  

<div class="code-runner">
<pre><code class="language-javascript">
// Example of a control structure in Ocean Adventure

let playerTouchesShark = true;

if (playerTouchesShark) {
    console.log("Player loses points!");
}
</code></pre>
</div>

---

### Iteration (Loops)

Iteration means repeating actions over and over again. In Ocean Adventure, loops were important because the game is always updating things like movement, enemies, and coins.

Here are some ways we used iteration:

- moving sharks toward the player every frame  
- checking all coins in the level  
- updating NPCs and enemies continuously  
- running the game update system  

<div class="code-runner">
<pre><code class="language-javascript">
// Example loop from Ocean Adventure style logic

let gameObjects = ["shark", "coin", "octopus"];

for (let obj of gameObjects) {
    console.log("Updating: " + obj);
}
</code></pre>
</div>

---

### Conditionals

Conditionals helped the game make decisions based on what was happening in the level. They made the game feel interactive instead of random.

We used conditionals for:

- detecting collisions with sharks or coins  
- giving points when coins are collected  
- ending the game when the player dies  
- controlling level changes  

<div class="code-runner">
<pre><code class="language-javascript">
// Example conditional (Ocean Adventure collision check)

let distance = 30;

if (distance < 40) {
    console.log("Collision happened!");
}
</code></pre>
</div>

---

### Nested Conditions

Nested conditions are when you put one condition inside another. We used this when the game needed to check multiple things before doing something.

We used nested conditions for:

- collision AND cooldown checks  
- making sure scoring system exists before adding points  
- preventing repeated damage every frame  

<div class="code-runner">
<pre><code class="language-javascript">
// Nested condition example

let distance = 30;
let cooldownActive = false;

if (distance < 40) {
    if (!cooldownActive) {
        console.log("Player takes damage!");
    }
}
</code></pre>
</div>

---

### Numbers

Numbers were used everywhere in Ocean Adventure to control movement, scoring, and positions.

We used numbers for:

- player speed  
- enemy speed  
- coin values (+10 points)  
- x and y positions  

<div class="code-runner">
<pre><code class="language-javascript">
// Numbers in Ocean Adventure

let speed = 6;
let score = 0;
let xPosition = 120;
let yPosition = 300;
</code></pre>
</div>

---

### Strings

Strings are just text. We used them to show messages and name objects in the game.

We used strings for:

- NPC dialogue  
- score messages like “+10 Points!”  
- object names like Shark or Octopus  

<div class="code-runner">
<pre><code class="language-javascript">
// Strings example

let message = "You collected a coin!";
console.log(message);
</code></pre>
</div>

---

### Booleans

Booleans are true or false values. We used them to control game states.

We used booleans for:

- checking if the player is alive  
- enemy cooldown systems  
- collision detection  
- game over state  

<div class="code-runner">
<pre><code class="language-javascript">
// Booleans in Ocean Adventure

let gameOver = false;
let isTouchingEnemy = true;
</code></pre>
</div>

---

### Arrays

Arrays helped us store multiple items like coins, enemies, and game objects.

We used arrays for:

- storing coins in the level  
- keeping track of enemies  
- looping through game objects  

<div class="code-runner">
<pre><code class="language-javascript">
// Arrays example

let coins = ["coin1", "coin2", "coin3"];

for (let coin of coins) {
    console.log("Checking " + coin);
}
</code></pre>
</div>

---

### Objects (JSON Style)

Objects helped us organize game data in a clean way so everything wasn’t messy.

We used objects for:

- player data (speed, position)  
- shark enemy data (damage, movement)  
- coin properties (value, location)  

<div class="code-runner">
<pre><code class="language-javascript">
// Object example (Ocean Adventure style)

let shark = {
    name: "Shark Enemy",
    speed: 3,
    damage: 10
};

console.log(shark.name);
</code></pre>
</div>

---

### Summary

All of these control structures and data types worked together to build Ocean Adventure. Loops kept the game running, conditionals made decisions, and data types stored everything like players, enemies, and scores.

Without these, the game wouldn’t move, react, or feel like a real game at all.


