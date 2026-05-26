---
layout: post
codemirror: true
title: CSSE Checklist
description: This checklist shows my progress over multiple important key concepts of CSSE through multiple examples of various projects as each section highlights the topics we implemented and used. Each button will take you to more information about the topic on a seperate page!
permalink: /csse-checklist
---

<div id="checklist-table"></div>

<script>
const data = [
  ["🎮 Object-Oriented Programming",
   "We used object oriented programming to organize our game into different classes like players, enemies, and coins so everything was easier to manage and reuse.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Writing Classes",
   "We used classes to structure game objects like players and enemies.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Methods & Parameters",
   "We used methods and parameters to control actions like movement and collisions.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Instantiation & Objects",
   "We used instantiation and objects to create reusable game elements that controlled movement, collisions, and player interactions throughout the game.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Inheritance (Basic)",
   "We used inheritance to allow game objects to share common properties like movement, position, and collision behavior.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Method Overriding",
   "We used method overriding to customize behaviors like movement, attacks, and collision responses for different game objects.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["Constructor Chaining",
   "We used constructor chaining to efficiently initialize shared properties across parent and child game classes.",
   "https://ishachaturvedi27.github.io/portfolio1/information-checklist"],

  ["⚙️ Control Structures",
   "Ocean Adventure Control Structures",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Iteration",
   "We used loops to repeatedly update enemies, coins, and game objects during gameplay.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Conditionals",
   "We used conditionals to detect collisions, control scoring, and react to player actions.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Nested Conditions",
   "We used nested conditions for cooldown systems, collision checks, and score protection.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["📦 Data Types",
   "Ocean Adventure Data Types",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Numbers",
   "We used numbers for score values, player movement speed, positions, and enemy movement.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Strings",
   "We used strings for NPC dialogue, object names, and score messages like +10 Points.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Booleans",
   "We used booleans for collision states, cooldown systems, and game over checks.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Arrays",
   "We used arrays to store enemies, coins, game objects, and level data.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["Objects (JSON)",
   "We used objects to organize player data, enemy properties, and scoring systems.",
   "https://ishachaturvedi27.github.io/portfolio1/control-structures"],

  ["➕ Operators",
   "We used operators like +, -, *, /, and logical comparisons to control scoring, movement, and game logic in Ocean Adventure.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["Mathematical Operators",
   "We used math operators for movement speed, scoring, distance calculations, and enemy tracking.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["String Operations",
   "We used string operations for score messages, NPC dialogue, and object names.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["Boolean Expressions",
   "We used boolean expressions for collisions, cooldown systems, and game logic checks.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["⌨️ Input/Output",
   "We used input and output in our game to take player controls (like keyboard input) and show results on the screen such as movement, scores, and game feedback.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["Keyboard Input",
   "We used keyboard input to move the octopus player with WASD controls in Ocean Adventure.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["Canvas Rendering",
   "We used canvas rendering to draw Ocean Adventure sprites, backgrounds, and animations on screen.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["GameEnv Configuration",
   "We used GameEnv configuration to set up levels, screen size, and game object behavior.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["API Integration",
   "We used API integration to support loading external game data and features.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["Asynchronous I/O",
   "We used asynchronous I/O so game assets load smoothly without freezing gameplay.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["JSON Parsing",
   "We used JSON parsing to organize player stats, enemy data, and level configurations.",
   "https://ishachaturvedi27.github.io/portfolio1/advanced-features"],

  ["📝 Documentation",
   "We used documentation to explain our code and make it easier to understand later.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Code Comments",
   "We used comments in our code to explain logic and make it easier to understand.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Mini-Lesson Documentation",
   "We documented mini-lessons to explain coding concepts and game features.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Code Highlights",
   "We highlighted important parts of our code to show key gameplay logic.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["🐞 Debugging",
   "We used debugging tools to find and fix problems in Ocean Adventure.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Console Debugging",
   "We used the console to test values and fix errors in Ocean Adventure.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Hit Box Visualization",
   "Ocean Adventure Hitbox Demo",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Source-Level Debugging",
   "We debugged code directly in the source to fix gameplay issues.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Network Debugging",
   "We checked network requests to make sure game data loaded correctly.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Application Debugging",
   "We tested the full application to find and fix gameplay bugs.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["Element Inspection",
   "We used inspect element tools to debug HTML and game UI issues.",
   "https://ishachaturvedi27.github.io/portfolio1/debugging-documentation"],

  ["✅ Testing & Verification",
   "We tested and checked our game carefully to make sure everything worked as expected. This helped us find bugs early and improve gameplay before publishing.",
   "https://ishachaturvedi27.github.io/portfolio1/testing-error-handling"],

  ["Gameplay Testing",
   "Ocean Adventure Gameplay Test",
   "https://pages.opencodingsociety.com/ocean-adventure"],

  ["Integration Testing",
   "We tested different parts of the game together to make sure everything worked correctly.",
   "https://ishachaturvedi27.github.io/portfolio1/testing-error-handling"],

  ["API Error Handling",
   "We used API error handling to prevent the game from crashing if data failed to load.",
   "https://ishachaturvedi27.github.io/portfolio1/testing-error-handling"]
];

const rainbowColors = ["#ff4d4d","#ff944d","#ffd24d","#66ff66","#4dd2ff","#6666ff","#cc66ff"];
const buttonColors = ["#ff4da6","#4dd2ff","#66ff66","#ffd24d","#cc66ff"];

const container = document.getElementById("checklist-table");
const table = document.createElement("table");

table.style.width = "100%";
table.style.borderCollapse = "collapse";
table.style.backgroundColor = "#0d1117";
table.style.color = "#ffffff";
table.style.fontFamily = "Arial, sans-serif";
table.style.borderRadius = "12px";
table.style.overflow = "hidden";

// HEADER
const headerRow = document.createElement("tr");
["Concept", "Implementation", "Explanation"].forEach((text, index) => {
  const th = document.createElement("th");
  th.textContent = text;
  th.style.padding = "14px";
  th.style.border = `2px solid ${rainbowColors[index + 1]}`;
  th.style.background = "linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet)";
  th.style.color = "white";
  th.style.fontWeight = "bold";
  th.style.fontSize = "16px";
  headerRow.appendChild(th);
});
table.appendChild(headerRow);

// ROWS
data.forEach((rowData, rowIndex) => {
  const row = document.createElement("tr");
  const borderColor = rainbowColors[rowIndex % rainbowColors.length];

  rowData.forEach((cellData, index) => {
    const cell = document.createElement("td");

    cell.style.border = `1px solid ${borderColor}`;
    cell.style.padding = "12px";
    cell.style.transition = "0.3s ease";
    cell.style.backgroundColor = "#161b22";
    cell.style.cursor = "pointer";

    if (index === 2 && cellData && cellData.startsWith("http")) {
      const link = document.createElement("a");
      link.href = cellData;
      link.target = "_blank";

      const button = document.createElement("div");
      button.textContent = "Open!";

      button.style.backgroundColor = buttonColors[rowIndex % buttonColors.length];
      button.style.color = "white";
      button.style.padding = "10px 20px";
      button.style.borderRadius = "5px";
      button.style.fontWeight = "bold";
      button.style.transition = "transform 0.2s, box-shadow 0.2s";
      button.style.display = "inline-block";

      button.addEventListener("mouseover", () => {
        button.style.transform = "scale(1.05)";
        button.style.boxShadow = "0 0 12px rgba(255,255,255,0.4)";
      });

      button.addEventListener("mouseout", () => {
        button.style.transform = "scale(1)";
        button.style.boxShadow = "none";
      });

      link.appendChild(button);
      cell.appendChild(link);
    } else {
      cell.textContent = cellData;
    }

    row.appendChild(cell);
  });

  table.appendChild(row);
});

container.appendChild(table);
</script>

### What Were a Few Things That We Struggled With?
Throughout the third trimester of this class my team ( me and joshika ) ran into quite a lot of issues but as we kept running into more we slowly started learning more and more. Below are a few examples of what we had problems with.

- game engine showing on the screen
- file orginization 
- config.yml conflicts 
- divergent branches 
- merging conflicts 
- pull requests 
- hidden syntax errors 
- repository orginzation 
- syncing forks 