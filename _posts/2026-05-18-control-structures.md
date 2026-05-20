---
layout: post
codemirror: true
title: Control Structures & Data Types (Ocean Adventure)
description: This explains how we used control structures, loops, and data types to make Ocean Adventure work.
permalink: /control-structures
---

### Control Structures

Control structures helped our Ocean Adventure game decide what should happen while the game was running. Instead of everything happening at once, the game checks different conditions and reacts to what the player is doing. This made the game feel way more interactive and realistic while we were coding it.

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

Iteration means repeating actions over and over again. In Ocean Adventure, loops were super important because the game constantly updates enemies, coins, movement, and animations while the player is playing. Without loops, we would have had to rewrite the same code again and again which would make the code messy and confusing.

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

Conditionals helped the game make decisions depending on what was happening in the level. They allowed the game to react differently based on player actions which made gameplay feel more real and less random. We used conditionals a lot for collisions, scoring, and level events.

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

Nested conditions are when one condition is placed inside another condition. We used these in Ocean Adventure whenever the game needed to check multiple things before doing an action. This helped stop bugs and made sure certain actions only happened at the correct time.

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

Numbers were used everywhere in Ocean Adventure because games rely on coordinates, movement, timing, and scoring systems. We used numbers to control things like player speed, enemy movement, health, and score values. Without numbers, the game objects would not know where to move or how fast to move.

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

Strings are basically text values in programming. We used strings throughout Ocean Adventure for dialogue, labels, and messages shown to the player during gameplay. Strings helped make the game feel more alive because players could actually see messages and names instead of just numbers.

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

Booleans are values that are either true or false. We used booleans a lot in Ocean Adventure to track game states and collisions. They helped the game know whether something was happening or not happening during gameplay.

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

Arrays helped us store multiple items together in one place. In Ocean Adventure, arrays were really useful because there were many enemies, coins, and game objects that needed to be updated constantly. Arrays made the code way more organized and easier to loop through.

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

Objects helped us organize information into groups instead of storing everything separately. We used objects for players, sharks, and collectibles because they could hold multiple properties in one place. This made the code cleaner and easier to understand while building the game.

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

### Data Types

Data types were really important in our Ocean Adventure game because they helped us store and organize different kinds of information while the game was running. We used data types for things like player movement, scores, enemy behavior, collisions, and interactions with NPCs. Different data types helped the game know what kind of information it was working with so everything functioned correctly.

Here are some ways we used data types in Ocean Adventure:

- numbers for player speed, score, and positions  
- strings for dialogue, labels, and game messages  
- booleans for checking collisions and game states  
- arrays for storing enemies, coins, and obstacles  
- objects for organizing player and shark information  

<div class="code-runner">
<pre><code class="language-javascript">
// Data types used in Ocean Adventure

// Number
let playerSpeed = 7;
let score = 50;

// String
let playerName = "Octo Explorer";

// Boolean
let gameOver = false;

// Array
let enemies = ["Shark", "Jellyfish", "Eel"];

// Object
let player = {
    name: "Octo Explorer",
    health: 100,
    speed: 7
};

console.log(player.name);
</code></pre>
</div>

---

### Summary

All of these control structures and data types worked together to build Ocean Adventure. Loops kept the game running, conditionals made decisions, and data types stored everything like players, enemies, and scores. Without these programming concepts, the game would not move, react, or feel like an actual playable game.


