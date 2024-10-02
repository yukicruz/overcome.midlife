---
layout: default
title: Core Values
permalink: /core-values/
---

<div class="content">
    <h1>Core Values</h1>
    <p>Identify your core values by answering the questions below.</p>
    <p>There will be three stages:
        <ol>
            <li>Select values that resonate with you.</li>
            <li>Prioritize values.</li>
            <li>See how your values are prioritized.</li>
        </ol>
    </p>
    
    <div id="progress">
      <div id="progress-bar"></div>
    </div>
    
    <div class="value-selection active" id="value-selection">
      <p id="value-text"></p>
      <button class="button" onclick="selectValue(true)">Yes</button>
      <button class="button" onclick="selectValue(false)">No</button>
    </div>
    
    <div class="comparison" id="comparison">
      <p>Choose which core value resonates with you more:</p>
      <button class="button" id="valueA" onclick="chooseValue('A')"></button>
      <button class="button" id="valueB" onclick="chooseValue('B')"></button>
    </div>
    
    <div class="results" id="results">
      <h2>The Core Values that Resonate with You</h2>
      <table>
        <thead>
          <tr>
            <th>Core Value</th>
            <th>Resonance (%)</th>
          </tr>
        </thead>
        <tbody id="results-table-body">
          <!-- Results will be populated here -->
        </tbody>
      </table>
    </div>
    
    <script>
      const values = [
        "Achievement", "Adventure", "Authenticity", "Balance", "Compassion",
        "Confidence", "Connection", "Contribution", "Courage", "Creativity",
        "Curiosity", "Determination", "Empathy", "Enthusiasm", "Equality",
        "Excellence", "Fairness", "Family", "Freedom", "Friendship",
        "Fun", "Growth", "Happiness", "Health", "Honesty",
        "Humor", "Independence", "Integrity", "Justice", "Kindness",
        "Knowledge", "Leadership", "Learning", "Love", "Loyalty",
        "Openness", "Optimism", "Passion", "Patience", "Peace",
        "Perseverance", "Respect", "Responsibility", "Security", "Service",
        "Simplicity", "Spirituality", "Trust", "Understanding", "Wisdom"
      ];
      
      let selectedValues = [];
      let currentIndex = 0;
      let comparisons = [];
      let comparisonCount = 0;
      const maxComparisons = 50;
      const maxTime = 120000; // 2 minutes in milliseconds
      let startTime;
      
      function updateProgress() {
        const progressBar = document.getElementById('progress-bar');
        progressBar.style.width = ((currentIndex / values.length) * 100) + '%';
      }
      
      function showNextValue() {
        if (currentIndex < values.length) {
          document.getElementById('value-text').innerText = `Does this value resonate with you? ${values[currentIndex]}`;
        } else {
          document.getElementById('value-selection').classList.remove('active');
          startComparison();
        }
        updateProgress();
      }
      
      function selectValue(isSelected) {
        if (isSelected) {
          selectedValues.push(values[currentIndex]);
        }
        currentIndex++;
        showNextValue();
      }
      
      function startComparison() {
        document.getElementById('comparison').classList.add('active');
        currentIndex = 0;
        comparisons = selectedValues.map(value => ({
          value: value,
          score: 0,
          comparisons: 0
        }));
        startTime = new Date().getTime();
        showComparison();
      }
      
      function showComparison() {
        const currentTime = new Date().getTime();
        if (comparisonCount >= maxComparisons || (currentTime - startTime) >= maxTime) {
          if (comparisons.some(comp => isNaN(comp.score / comp.comparisons))) {
            comparisonCount = 0;
            startTime = new Date().getTime();
            showComparison();
          } else {
            finishQuestionnaire();
          }
          return;
        }
        
        if (selectedValues.length > 1) {
          const valueA = selectedValues[Math.floor(Math.random() * selectedValues.length)];
          let valueB = valueA;
          while (valueB === valueA) {
            valueB = selectedValues[Math.floor(Math.random() * selectedValues.length)];
          }
          document.getElementById('valueA').innerText = valueA;
          document.getElementById('valueB').innerText = valueB;
          comparisonCount++;
        } else {
          finishQuestionnaire();
        }
      }
      
      function chooseValue(choice) {
        const valueA = document.getElementById('valueA').innerText;
        const valueB = document.getElementById('valueB').innerText;
        const winner = (choice === 'A') ? valueA : valueB;
        const loser = (choice === 'A') ? valueB : valueA;
        
        comparisons.forEach(comp => {
          if (comp.value === winner) {
            comp.score++;
          }
          if (comp.value === winner || comp.value === loser) {
            comp.comparisons++;
          }
        });
        
        showComparison();
      }
      
      function finishQuestionnaire() {
        document.getElementById('comparison').classList.remove('active');
        const resultsTableBody = document.getElementById('results-table-body');
        resultsTableBody.innerHTML = '';
        
        comparisons.sort((a, b) => (b.score / b.comparisons) - (a.score / a.comparisons));
        
        comparisons.forEach(comp => {
          const row = document.createElement('tr');
          const valueCell = document.createElement('td');
          valueCell.innerText = comp.value;
          const scoreCell = document.createElement('td');
          const resonance = ((comp.score / comp.comparisons) * 100).toFixed(2);
          scoreCell.innerText = isNaN(resonance) ? '0.00' : resonance;
          row.appendChild(valueCell);
          row.appendChild(scoreCell);
          resultsTableBody.appendChild(row);
        });
        
        document.getElementById('results').classList.add('active');
      }
      
      showNextValue();
    </script>
</div>
