---
layout: post
codemirror: true
title: CSSE Checklist
description: This checklist shows my progress over multiple important key concepts of CSSE through multiple examples of various projects as each section highlights the topics we implemented and used.
permalink: /csse-checklist
---

<div id="checklist-table"></div>

<script>
const data = [
  ["🎮 Object-Oriented Programming", "", ""],

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

  ["📦 Data Types", "", ""],

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

  ["➕ Operators", "", ""],
  ["Mathematical", "", ""],
  ["String Operations", "", ""],
  ["Boolean Expressions", "", ""],

  ["⌨️ Input/Output", "", ""],
  ["Keyboard Input", "", ""],
  ["Canvas Rendering", "", ""],
  ["GameEnv Configuration", "", ""],
  ["API Integration", "", ""],
  ["Asynchronous I/O", "", ""],
  ["JSON Parsing", "", ""],

  ["📝 Documentation", "", ""],
  ["Code Comments", "", ""],
  ["Mini-Lesson Documentation", "", ""],
  ["Code Highlights", "", ""],

  ["🐞 Debugging", "", ""],

  ["Console Debugging", "", ""],

  ["Hit Box Visualization",
   "Ocean Adventure Hitbox Demo",
   "https://pages.opencodingsociety.com/ocean-adventure"],

  ["Source-Level Debugging", "", ""],
  ["Network Debugging", "", ""],
  ["Application Debugging", "", ""],
  ["Element Inspection", "", ""],

  ["✅ Testing & Verification", "", ""],

  ["Gameplay Testing",
   "Ocean Adventure Gameplay Test",
   "https://pages.opencodingsociety.com/ocean-adventure"],

  ["Integration Testing", "", ""],
  ["API Error Handling", "", ""]
];

const rainbowColors = [
  "#ff4d4d",
  "#ff944d",
  "#ffd24d",
  "#66ff66",
  "#4dd2ff",
  "#6666ff",
  "#cc66ff"
];

// alternating button colors
const buttonColors = [
  "#ff4da6",
  "#4dd2ff",
  "#66ff66",
  "#ffd24d",
  "#cc66ff"
];

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
  th.style.background =
    "linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet)";
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

    // BUTTON LINKS
    if (index === 2 && cellData && cellData.startsWith("http")) {
      const link = document.createElement("a");
      link.href = cellData;
      link.target = "_blank";
      link.style.textDecoration = "none";

      const button = document.createElement("div");
      button.textContent = "Open!";

      // alternating button colors
      button.style.backgroundColor =
        buttonColors[rowIndex % buttonColors.length];

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

    // rainbow hover effect
    cell.addEventListener("mouseover", () => {
      if (!cell.querySelector("a")) {
        cell.style.backgroundColor = borderColor;
        cell.style.color = "#000";
      }
    });

    cell.addEventListener("mouseout", () => {
      if (!cell.querySelector("a")) {
        cell.style.backgroundColor = "#161b22";
        cell.style.color = "#fff";
      }
    });

    row.appendChild(cell);
  });

  // section headers
  if (
      rowData[1] === "" &&
      rowData[2] === "" &&
      (
        rowData[0].includes("🎮") ||
        rowData[0].includes("⚙️") ||
        rowData[0].includes("📦") ||
        rowData[0].includes("➕") ||
        rowData[0].includes("⌨️") ||
        rowData[0].includes("📝") ||
        rowData[0].includes("🐞") ||
        rowData[0].includes("✅")
      )
    ) {
    row.style.fontWeight = "bold";
    row.style.fontSize = "17px";
    row.style.backgroundColor = "#111827";
  }

  table.appendChild(row);
});

container.appendChild(table);
</script>