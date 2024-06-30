---
layout: default
title: Key Life Domains
permalink: /key-life-domains/
---

# Key Life Domains

Here you can rate each key life domain on a scale of 1 to 10.

## Financial
<input type="range" min="1" max="10" value="5" class="slider" id="financialRange">
<p>Value: <span id="financialValue"></span></p>

## Social/Relationships
<input type="range" min="1" max="10" value="5" class="slider" id="socialRange">
<p>Value: <span id="socialValue"></span></p>

## Physical Health
<input type="range" min="1" max="10" value="5" class="slider" id="physicalRange">
<p>Value: <span id="physicalValue"></span></p>

## Mental/Emotional
<input type="range" min="1" max="10" value="5" class="slider" id="mentalRange">
<p>Value: <span id="mentalValue"></span></p>

## Spiritual
<input type="range" min="1" max="10" value="5" class="slider" id="spiritualRange">
<p>Value: <span id="spiritualValue"></span></p>

## Environment
<input type="range" min="1" max="10" value="5" class="slider" id="environmentRange">
<p>Value: <span id="environmentValue"></span></p>

## Career
<input type="range" min="1" max="10" value="5" class="slider" id="careerRange">
<p>Value: <span id="careerValue"></span></p>

<script>
document.addEventListener("DOMContentLoaded", function() {
  var sliders = document.querySelectorAll(".slider");
  sliders.forEach(function(slider) {
    var valueDisplay = document.getElementById(slider.id.replace("Range", "Value"));
    valueDisplay.innerHTML = slider.value; // Display the default slider value

    slider.oninput = function() {
      valueDisplay.innerHTML = this.value;
    };
  });
});
</script>
