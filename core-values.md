---
layout: default
title: Core Values
permalink: /core-values/
---

<h1>Core Values</h1>
<p>Identify your core values by answering the questions below.</p>

<div id="core-values-container">
    <div id="question"></div>
    <div id="buttons">
        <button id="value1" onclick="selectValue(1)"></button>
        <button id="value2" onclick="selectValue(2)"></button>
    </div>
    <div id="result" style="display: none;">
        <h2>Your Core Values from Most to Least Important</h2>
        <ol id="values-list"></ol>
    </div>
</div>

<script>
    const coreValues = [
        "Integrity",
        "Honesty",
        "Loyalty",
        "Respect",
        "Responsibility",
        "Compassion",
        "Fairness",
        "Commitment",
        "Perseverance",
        "Courage"
    ];

    let currentIndex = 0;
    const valuesCount = coreValues.length;
    const userPreferences = Array(valuesCount).fill(0).map((_, index) => index);

    function shuffle(array) {
        for (let i = array.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [array[i], array[j]] = [array[j], array[i]];
        }
    }

    function showQuestion() {
        if (currentIndex < valuesCount - 1) {
            document.getElementById('value1').innerText = coreValues[userPreferences[currentIndex]];
            document.getElementById('value2').innerText = coreValues[userPreferences[currentIndex + 1]];
            document.getElementById('question').innerText = `Which is more important to you?`;
        } else {
            showResult();
        }
    }

    function selectValue(selectedIndex) {
        if (selectedIndex === 1) {
            [userPreferences[currentIndex], userPreferences[currentIndex + 1]] = [userPreferences[currentIndex + 1], userPreferences[currentIndex]];
        }
        currentIndex++;
        showQuestion();
    }

    function showResult() {
        document.getElementById('buttons').style.display = 'none';
        const resultContainer = document.getElementById('result');
        resultContainer.style.display = 'block';
        const valuesList = document.getElementById('values-list');
        userPreferences.forEach(index => {
            const listItem = document.createElement('li');
            listItem.innerText = coreValues[index];
            valuesList.appendChild(listItem);
        });
    }

    shuffle(userPreferences);
    showQuestion();
</script>
