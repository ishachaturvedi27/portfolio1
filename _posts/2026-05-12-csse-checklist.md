---
layout: post
codemirror: true
title: CSSE Checklist
description: This checklist shows my progress over mltiple important key concepts of CSSE through multiple examples of various projects as each seciton highlights the topics we implemented and used. 
permalink: /csse-checklist
---

<div id="checklist-table"></div>

<script>
const data = [
  ["🎮 Object-Oriented Programming", "", ""],
  ["Writing Classes", "", ""],
  ["Methods & Parameters", "", ""],
  ["Instantiation & Objects", "", ""],
  ["Inheritance (Basic)", "", ""],
  ["Method Overriding", "", ""],
  ["Constructor Chaining", "", ""],

  ["⚙️ Control Structures", "", ""],
  ["Iteration", "", ""],
  ["Conditionals", "", ""],
  ["Nested Conditions", "", ""],

  ["📦 Data Types", "", ""],
  ["Numbers", "", ""],
  ["Strings", "", ""],
  ["Booleans", "", ""],
  ["Arrays", "", ""],
  ["Objects (JSON)", "", ""],

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
  ["Hit Box Visualization", "", ""],
  ["Source-Level Debugging", "", ""],
  ["Network Debugging", "", ""],
  ["Application Debugging", "", ""],
  ["Element Inspection", "", ""],

  ["✅ Testing & Verification", "", ""],
  ["Gameplay Testing", "", ""],
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

["Concept", "Project Evidence Required", "Assessment Method"].forEach((text, index) => {
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

  rowData.forEach((cellData) => {
    const cell = document.createElement("td");

    cell.style.border = `1px solid ${borderColor}`;
    cell.style.padding = "12px";
    cell.style.transition = "0.3s ease";
    cell.style.backgroundColor = "#161b22";

    cell.textContent = cellData;

    // rainbow hover effect
    cell.addEventListener("mouseover", () => {
      cell.style.backgroundColor = borderColor;
      cell.style.color = "#000";
    });

    cell.addEventListener("mouseout", () => {
      cell.style.backgroundColor = "#161b22";
      cell.style.color = "#fff";
    });

    row.appendChild(cell);
  });

  // section headers
  if (rowData[1] === "" && rowData[2] === "" && rowData[0].includes(" ")) {
    row.style.fontWeight = "bold";
    row.style.fontSize = "17px";
  }

  table.appendChild(row);
});

container.appendChild(table);
</script>