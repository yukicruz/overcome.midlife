---
layout: default
title: Life Satisfaction Survey
permalink: /life-satisfaction-survey/
---

<h1>Life Satisfaction Survey</h1>
<p>Take this survey to see which of your life areas are doing great and which might need work.</p>

<style>
    body { font-family: Arial, sans-serif; }
    .section { margin: 20px 0; }
    .question { margin: 10px 0; }
    .stars { display: inline-block; cursor: pointer; }
    .stars input[type="radio"] { display: none; }
    .stars label { font-size: 24px; color: lightgray; }
    .stars input[type="radio"]:checked ~ label { color: lightgray; }
    .stars input[type="radio"]:checked + label,
    .stars input[type="radio"]:checked + label ~ label { color: gold; }
    .stars label:hover,
    .stars label:hover ~ label { color: gold; }
</style>

<body>

    <!-- Life Area #1: Career and Work -->
    <div class="section" id="career">
        <h2>1. Career and Work</h2>
        <div class="question">
            <p>How satisfied are you with your current job or career path?</p>
            <div class="stars">
                <input type="radio" id="career1-1" name="career1" value="1"><label for="career1-1">★</label>
                <input type="radio" id="career1-2" name="career1" value="2"><label for="career1-2">★</label>
                <input type="radio" id="career1-3" name="career1" value="3"><label for="career1-3">★</label>
                <input type="radio" id="career1-4" name="career1" value="4"><label for="career1-4">★</label>
                <input type="radio" id="career1-5" name="career1" value="5"><label for="career1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you feel you have opportunities for growth and development in your career?</p>
            <div class="stars">
                <input type="radio" id="career2-1" name="career2" value="1"><label for="career2-1">★</label>
                <input type="radio" id="career2-2" name="career2" value="2"><label for="career2-2">★</label>
                <input type="radio" id="career2-3" name="career2" value="3"><label for="career2-3">★</label>
                <input type="radio" id="career2-4" name="career2" value="4"><label for="career2-4">★</label>
                <input type="radio" id="career2-5" name="career2" value="5"><label for="career2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How meaningful and fulfilling do you find your work?</p>
            <div class="stars">
                <input type="radio" id="career3-1" name="career3" value="1"><label for="career3-1">★</label>
                <input type="radio" id="career3-2" name="career3" value="2"><label for="career3-2">★</label>
                <input type="radio" id="career3-3" name="career3" value="3"><label for="career3-3">★</label>
                <input type="radio" id="career3-4" name="career3" value="4"><label for="career3-4">★</label>
                <input type="radio" id="career3-5" name="career3" value="5"><label for="career3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="career-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="relationships">
        <h2>2. Relationships and Social Connections</h2>
        <div class="question">
            <p>Are your personal relationships supportive and enriching?</p>
            <div class="stars">
                <input type="radio" id="relationships1-1" name="relationships1" value="1"><label for="relationships1-1">★</label>
                <input type="radio" id="relationships1-2" name="relationships1" value="2"><label for="relationships1-2">★</label>
                <input type="radio" id="relationships1-3" name="relationships1" value="3"><label for="relationships1-3">★</label>
                <input type="radio" id="relationships1-4" name="relationships1" value="4"><label for="relationships1-4">★</label>
                <input type="radio" id="relationships1-5" name="relationships1" value="5"><label for="relationships1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you feel connected to a community or social network?</p>
            <div class="stars">
                <input type="radio" id="relationships2-1" name="relationships2" value="1"><label for="relationships2-1">★</label>
                <input type="radio" id="relationships2-2" name="relationships2" value="2"><label for="relationships2-2">★</label>
                <input type="radio" id="relationships2-3" name="relationships2" value="3"><label for="relationships2-3">★</label>
                <input type="radio" id="relationships2-4" name="relationships2" value="4"><label for="relationships2-4">★</label>
                <input type="radio" id="relationships2-5" name="relationships2" value="5"><label for="relationships2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How satisfied are you with the quality of your interactions with family and friends?</p>
            <div class="stars">
                <input type="radio" id="relationships3-1" name="relationships3" value="1"><label for="relationships3-1">★</label>
                <input type="radio" id="relationships3-2" name="relationships3" value="2"><label for="relationships3-2">★</label>
                <input type="radio" id="relationships3-3" name="relationships3" value="3"><label for="relationships3-3">★</label>
                <input type="radio" id="relationships3-4" name="relationships3" value="4"><label for="relationships3-4">★</label>
                <input type="radio" id="relationships3-5" name="relationships3" value="5"><label for="relationships3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="relationships-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="health">
        <h2>3. Health and Wellness</h2>
        <div class="question">
            <p>How satisfied are you with your physical health and fitness?</p>
            <div class="stars">
                <input type="radio" id="health1-1" name="health1" value="1"><label for="health1-1">★</label>
                <input type="radio" id="health1-2" name="health1" value="2"><label for="health1-2">★</label>
                <input type="radio" id="health1-3" name="health1" value="3"><label for="health1-3">★</label>
                <input type="radio" id="health1-4" name="health1" value="4"><label for="health1-4">★</label>
                <input type="radio" id="health1-5" name="health1" value="5"><label for="health1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you engage in regular self-care practices for your mental well-being?</p>
            <div class="stars">
                <input type="radio" id="health2-1" name="health2" value="1"><label for="health2-1">★</label>
                <input type="radio" id="health2-2" name="health2" value="2"><label for="health2-2">★</label>
                <input type="radio" id="health2-3" name="health2" value="3"><label for="health2-3">★</label>
                <input type="radio" id="health2-4" name="health2" value="4"><label for="health2-4">★</label>
                <input type="radio" id="health2-5" name="health2" value="5"><label for="health2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How balanced and healthy is your diet and nutrition?</p>
            <div class="stars">
                <input type="radio" id="health3-1" name="health3" value="1"><label for="health3-1">★</label>
                <input type="radio" id="health3-2" name="health3" value="2"><label for="health3-2">★</label>
                <input type="radio" id="health3-3" name="health3" value="3"><label for="health3-3">★</label>
                <input type="radio" id="health3-4" name="health3" value="4"><label for="health3-4">★</label>
                <input type="radio" id="health3-5" name="health3" value="5"><label for="health3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="health-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="personal-growth">
        <h2>4. Personal Growth and Learning</h2>
        <div class="question">
            <p>Are you satisfied with your opportunities for personal development and learning?</p>
            <div class="stars">
                <input type="radio" id="personal-growth1-1" name="personal-growth1" value="1"><label for="personal-growth1-1">★</label>
                <input type="radio" id="personal-growth1-2" name="personal-growth1" value="2"><label for="personal-growth1-2">★</label>
                <input type="radio" id="personal-growth1-3" name="personal-growth1" value="3"><label for="personal-growth1-3">★</label>
                <input type="radio" id="personal-growth1-4" name="personal-growth1" value="4"><label for="personal-growth1-4">★</label>
                <input type="radio" id="personal-growth1-5" name="personal-growth1" value="5"><label for="personal-growth1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you feel you are growing and evolving as a person?</p>
            <div class="stars">
                <input type="radio" id="personal-growth2-1" name="personal-growth2" value="1"><label for="personal-growth2-1">★</label>
                <input type="radio" id="personal-growth2-2" name="personal-growth2" value="2"><label for="personal-growth2-2">★</label>
                <input type="radio" id="personal-growth2-3" name="personal-growth2" value="3"><label for="personal-growth2-3">★</label>
                <input type="radio" id="personal-growth2-4" name="personal-growth2" value="4"><label for="personal-growth2-4">★</label>
                <input type="radio" id="personal-growth2-5" name="personal-growth2" value="5"><label for="personal-growth2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How often do you engage in activities that challenge you and help you grow?</p>
            <div class="stars">
                <input type="radio" id="personal-growth3-1" name="personal-growth3" value="1"><label for="personal-growth3-1">★</label>
                <input type="radio" id="personal-growth3-2" name="personal-growth3" value="2"><label for="personal-growth3-2">★</label>
                <input type="radio" id="personal-growth3-3" name="personal-growth3" value="3"><label for="personal-growth3-3">★</label>
                <input type="radio" id="personal-growth3-4" name="personal-growth3" value="4"><label for="personal-growth3-4">★</label>
                <input type="radio" id="personal-growth3-5" name="personal-growth3" value="5"><label for="personal-growth3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="personal-growth-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="financial-stability">
        <h2>5. Financial Stability and Resources</h2>
        <div class="question">
            <p>Do you feel secure in your financial situation?</p>
            <div class="stars">
                <input type="radio" id="financial-stability1-1" name="financial-stability1" value="1"><label for="financial-stability1-1">★</label>
                <input type="radio" id="financial-stability1-2" name="financial-stability1" value="2"><label for="financial-stability1-2">★</label>
                <input type="radio" id="financial-stability1-3" name="financial-stability1" value="3"><label for="financial-stability1-3">★</label>
                <input type="radio" id="financial-stability1-4" name="financial-stability1" value="4"><label for="financial-stability1-4">★</label>
                <input type="radio" id="financial-stability1-5" name="financial-stability1" value="5"><label for="financial-stability1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Are you able to meet your financial goals and obligations comfortably?</p>
            <div class="stars">
                <input type="radio" id="financial-stability2-1" name="financial-stability2" value="1"><label for="financial-stability2-1">★</label>
                <input type="radio" id="financial-stability2-2" name="financial-stability2" value="2"><label for="financial-stability2-2">★</label>
                <input type="radio" id="financial-stability2-3" name="financial-stability2" value="3"><label for="financial-stability2-3">★</label>
                <input type="radio" id="financial-stability2-4" name="financial-stability2" value="4"><label for="financial-stability2-4">★</label>
                <input type="radio" id="financial-stability2-5" name="financial-stability2" value="5"><label for="financial-stability2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How satisfied are you with your ability to manage and save money?</p>
            <div class="stars">
                <input type="radio" id="financial-stability3-1" name="financial-stability3" value="1"><label for="financial-stability3-1">★</label>
                <input type="radio" id="financial-stability3-2" name="financial-stability3" value="2"><label for="financial-stability3-2">★</label>
                <input type="radio" id="financial-stability3-3" name="financial-stability3" value="3"><label for="financial-stability3-3">★</label>
                <input type="radio" id="financial-stability3-4" name="financial-stability3" value="4"><label for="financial-stability3-4">★</label>
                <input type="radio" id="financial-stability3-5" name="financial-stability3" value="5"><label for="financial-stability3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="financial-stability-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="leisure">
        <h2>6. Leisure and Recreation</h2>
        <div class="question">
            <p>Do you have enough time for hobbies and activities that you enjoy?</p>
            <div class="stars">
                <input type="radio" id="leisure1-1" name="leisure1" value="1"><label for="leisure1-1">★</label>
                <input type="radio" id="leisure1-2" name="leisure1" value="2"><label for="leisure1-2">★</label>
                <input type="radio" id="leisure1-3" name="leisure1" value="3"><label for="leisure1-3">★</label>
                <input type="radio" id="leisure1-4" name="leisure1" value="4"><label for="leisure1-4">★</label>
                <input type="radio" id="leisure1-5" name="leisure1" value="5"><label for="leisure1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Are you able to relax and recharge effectively during your free time?</p>
            <div class="stars">
                <input type="radio" id="leisure2-1" name="leisure2" value="1"><label for="leisure2-1">★</label>
                <input type="radio" id="leisure2-2" name="leisure2" value="2"><label for="leisure2-2">★</label>
                <input type="radio" id="leisure2-3" name="leisure2" value="3"><label for="leisure2-3">★</label>
                <input type="radio" id="leisure2-4" name="leisure2" value="4"><label for="leisure2-4">★</label>
                <input type="radio" id="leisure2-5" name="leisure2" value="5"><label for="leisure2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How satisfied are you with the variety and quality of your leisure activities?</p>
            <div class="stars">
                <input type="radio" id="leisure3-1" name="leisure3" value="1"><label for="leisure3-1">★</label>
                <input type="radio" id="leisure3-2" name="leisure3" value="2"><label for="leisure3-2">★</label>
                <input type="radio" id="leisure3-3" name="leisure3" value="3"><label for="leisure3-3">★</label>
                <input type="radio" id="leisure3-4" name="leisure3" value="4"><label for="leisure3-4">★</label>
                <input type="radio" id="leisure3-5" name="leisure3" value="5"><label for="leisure3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="leisure-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="living-environment">
        <h2>7. Living Environment</h2>
        <div class="question">
            <p>Are you satisfied with your living conditions and environment?</p>
            <div class="stars">
                <input type="radio" id="living-environment1-1" name="living-environment1" value="1"><label for="living-environment1-1">★</label>
                <input type="radio" id="living-environment1-2" name="living-environment1" value="2"><label for="living-environment1-2">★</label>
                <input type="radio" id="living-environment1-3" name="living-environment1" value="3"><label for="living-environment1-3">★</label>
                <input type="radio" id="living-environment1-4" name="living-environment1" value="4"><label for="living-environment1-4">★</label>
                <input type="radio" id="living-environment1-5" name="living-environment1" value="5"><label for="living-environment1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you feel safe and comfortable in your home?</p>
            <div class="stars">
                <input type="radio" id="living-environment2-1" name="living-environment2" value="1"><label for="living-environment2-1">★</label>
                <input type="radio" id="living-environment2-2" name="living-environment2" value="2"><label for="living-environment2-2">★</label>
                <input type="radio" id="living-environment2-3" name="living-environment2" value="3"><label for="living-environment2-3">★</label>
                <input type="radio" id="living-environment2-4" name="living-environment2" value="4"><label for="living-environment2-4">★</label>
                <input type="radio" id="living-environment2-5" name="living-environment2" value="5"><label for="living-environment2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How content are you with your neighborhood and local community?</p>
            <div class="stars">
                <input type="radio" id="living-environment3-1" name="living-environment3" value="1"><label for="living-environment3-1">★</label>
                <input type="radio" id="living-environment3-2" name="living-environment3" value="2"><label for="living-environment3-2">★</label>
                <input type="radio" id="living-environment3-3" name="living-environment3" value="3"><label for="living-environment3-3">★</label>
                <input type="radio" id="living-environment3-4" name="living-environment3" value="4"><label for="living-environment3-4">★</label>
                <input type="radio" id="living-environment3-5" name="living-environment3" value="5"><label for="living-environment3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="living-environment-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="spirituality">
        <h2>8. Spirituality and Meaning</h2>
        <div class="question">
            <p>Do you feel a sense of purpose and meaning in your life?</p>
            <div class="stars">
                <input type="radio" id="spirituality1-1" name="spirituality1" value="1"><label for="spirituality1-1">★</label>
                <input type="radio" id="spirituality1-2" name="spirituality1" value="2"><label for="spirituality1-2">★</label>
                <input type="radio" id="spirituality1-3" name="spirituality1" value="3"><label for="spirituality1-3">★</label>
                <input type="radio" id="spirituality1-4" name="spirituality1" value="4"><label for="spirituality1-4">★</label>
                <input type="radio" id="spirituality1-5" name="spirituality1" value="5"><label for="spirituality1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Are you connected to a spiritual or philosophical belief system that supports you?</p>
            <div class="stars">
                <input type="radio" id="spirituality2-1" name="spirituality2" value="1"><label for="spirituality2-1">★</label>
                <input type="radio" id="spirituality2-2" name="spirituality2" value="2"><label for="spirituality2-2">★</label>
                <input type="radio" id="spirituality2-3" name="spirituality2" value="3"><label for="spirituality2-3">★</label>
                <input type="radio" id="spirituality2-4" name="spirituality2" value="4"><label for="spirituality2-4">★</label>
                <input type="radio" id="spirituality2-5" name="spirituality2" value="5"><label for="spirituality2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>How often do you engage in practices that nurture your spiritual well-being?</p>
            <div class="stars">
                <input type="radio" id="spirituality3-1" name="spirituality3" value="1"><label for="spirituality3-1">★</label>
                <input type="radio" id="spirituality3-2" name="spirituality3" value="2"><label for="spirituality3-2">★</label>
                <input type="radio" id="spirituality3-3" name="spirituality3" value="3"><label for="spirituality3-3">★</label>
                <input type="radio" id="spirituality3-4" name="spirituality3" value="4"><label for="spirituality3-4">★</label>
                <input type="radio" id="spirituality3-5" name="spirituality3" value="5"><label for="spirituality3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="spirituality-score">0</span> / 15</p>
    </div>
    
    <div class="section" id="overall-happiness">
        <h2>9. Overall Happiness</h2>
        <div class="question">
            <p>How happy do you feel in general?</p>
            <div class="stars">
                <input type="radio" id="overall-happiness1-1" name="overall-happiness1" value="1"><label for="overall-happiness1-1">★</label>
                <input type="radio" id="overall-happiness1-2" name="overall-happiness1" value="2"><label for="overall-happiness1-2">★</label>
                <input type="radio" id="overall-happiness1-3" name="overall-happiness1" value="3"><label for="overall-happiness1-3">★</label>
                <input type="radio" id="overall-happiness1-4" name="overall-happiness1" value="4"><label for="overall-happiness1-4">★</label>
                <input type="radio" id="overall-happiness1-5" name="overall-happiness1" value="5"><label for="overall-happiness1-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Are you content with your life as a whole?</p>
            <div class="stars">
                <input type="radio" id="overall-happiness2-1" name="overall-happiness2" value="1"><label for="overall-happiness2-1">★</label>
                <input type="radio" id="overall-happiness2-2" name="overall-happiness2" value="2"><label for="overall-happiness2-2">★</label>
                <input type="radio" id="overall-happiness2-3" name="overall-happiness2" value="3"><label for="overall-happiness2-3">★</label>
                <input type="radio" id="overall-happiness2-4" name="overall-happiness2" value="4"><label for="overall-happiness2-4">★</label>
                <input type="radio" id="overall-happiness2-5" name="overall-happiness2" value="5"><label for="overall-happiness2-5">★</label>
            </div>
        </div>
        <div class="question">
            <p>Do you wake up feeling positive and hopeful about the day ahead?</p>
            <div class="stars">
                <input type="radio" id="overall-happiness3-1" name="overall-happiness3" value="1"><label for="overall-happiness3-1">★</label>
                <input type="radio" id="overall-happiness3-2" name="overall-happiness3" value="2"><label for="overall-happiness3-2">★</label>
                <input type="radio" id="overall-happiness3-3" name="overall-happiness3" value="3"><label for="overall-happiness3-3">★</label>
                <input type="radio" id="overall-happiness3-4" name="overall-happiness3" value="4"><label for="overall-happiness3-4">★</label>
                <input type="radio" id="overall-happiness3-5" name="overall-happiness3" value="5"><label for="overall-happiness3-5">★</label>
            </div>
        </div>
        <p><strong>Total Score:</strong> <span id="overall-happiness-score">0</span> / 15</p>
    </div>
    
    
    <!-- Repeat similar blocks for other life areas -->
    
    <!-- Scripts to handle the score calculation -->
    <script>
        document.querySelectorAll('.section').forEach(section => {
            section.addEventListener('change', () => {
                let totalScore = 0;
                section.querySelectorAll('input[type="radio"]:checked').forEach(input => {
                    totalScore += parseInt(input.value);
                });
                section.querySelector('span').textContent = totalScore;
            });
    
            section.querySelectorAll('.stars label').forEach(label => {
                label.addEventListener('click', function() {
                    let allLabels = Array.from(this.parentNode.querySelectorAll('label'));
                    let index = allLabels.indexOf(this);
                    allLabels.forEach((lbl, i) => {
                        lbl.style.color = i <= index ? 'gold' : 'lightgray';
                    });
                });
    
                label.addEventListener('mouseover', function() {
                    let allLabels = Array.from(this.parentNode.querySelectorAll('label'));
                    let index = allLabels.indexOf(this);
                    allLabels.forEach((lbl, i) => {
                        lbl.style.color = i <= index ? 'gold' : 'lightgray';
                    });
                });
    
                label.addEventListener('mouseout', function() {
                    let allLabels = Array.from(this.parentNode.querySelectorAll('label'));
                    let checkedRadio = this.parentNode.querySelector('input[type="radio"]:checked');
                    let checkedIndex = checkedRadio ? allLabels.indexOf(checkedRadio.nextElementSibling) : -1;
                    allLabels.forEach((lbl, i) => {
                        lbl.style.color = i <= checkedIndex ? 'gold' : 'lightgray';
                    });
                });
            });
        });
    </script>
    
    <!-- Button and Table Placeholder -->
    <p>Want to see how your life areas compare?</p>
    <button id="calculateBtn">Calculate</button>
    
    <table id="resultsTable" style="display:none; margin-top:20px; border-collapse: collapse; width: 100%;">
        <thead>
            <tr>
                <th style="border: 1px solid #ddd; padding: 8px;">Rank</th>
                <th style="border: 1px solid #ddd; padding: 8px;">Life Area</th>
                <th style="border: 1px solid #ddd; padding: 8px;">Life Area Score</th>
            </tr>
        </thead>
        <tbody>
            <!-- Results will be inserted here -->
        </tbody>
    </table>
    
    <script>
        document.getElementById('calculateBtn').addEventListener('click', function() {
            const lifeAreas = [
                { id: 'career', name: 'Career and Work', score: parseInt(document.getElementById('career-score').textContent) },
                { id: 'relationships', name: 'Relationships and Social Connections', score: parseInt(document.getElementById('relationships-score').textContent) },
                { id: 'health', name: 'Health and Wellness', score: parseInt(document.getElementById('health-score').textContent) },
                { id: 'personal-growth', name: 'Personal Growth and Learning', score: parseInt(document.getElementById('personal-growth-score').textContent) },
                { id: 'financial-stability', name: 'Financial Stability and Resources', score: parseInt(document.getElementById('financial-stability-score').textContent) },
                { id: 'leisure', name: 'Leisure and Recreation', score: parseInt(document.getElementById('leisure-score').textContent) },
                { id: 'living-environment', name: 'Living Environment', score: parseInt(document.getElementById('living-environment-score').textContent) },
                { id: 'spirituality', name: 'Spirituality and Meaning', score: parseInt(document.getElementById('spirituality-score').textContent) },
                { id: 'overall-happiness', name: 'Overall Happiness', score: parseInt(document.getElementById('overall-happiness-score').textContent) },
            ];
    
            lifeAreas.sort((a, b) => b.score - a.score);
    
            const resultsTable = document.getElementById('resultsTable');
            const tbody = resultsTable.querySelector('tbody');
            tbody.innerHTML = '';
    
            lifeAreas.forEach((area, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td style="border: 1px solid #ddd; padding: 8px;">${index + 1}</td>
                    <td style="border: 1px solid #ddd; padding: 8px;">${area.name}</td>
                    <td style="border: 1px solid #ddd; padding: 8px;">${area.score}</td>
                `;
                tbody.appendChild(row);
            });
    
            resultsTable.style.display = 'table';
        });
    </script>

</body>
