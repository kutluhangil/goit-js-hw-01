<h1>📘 JavaScript Homework 1</h1>

<p>This repository contains solutions for <b>3 tasks</b> focused on <b>variables, data types, and basic functions</b> in JavaScript. Each task is implemented in a separate file (<code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code>).</p>

<hr/>

<h2>🔹 Task 1: Droid Order (<code>task-1.js</code>)</h2>
<p>A function that calculates the total cost of droids and returns a formatted message.</p>

<pre>
function makeTransaction(quantity, pricePerDroid) {
  const totalPrice = quantity * pricePerDroid;
  return `You ordered ${quantity} droids worth ${totalPrice} credits!`;
}
</pre>

<h3>✅ Test Results</h3>
<pre>
makeTransaction(5, 3000) → "You ordered 5 droids worth 15000 credits!"
makeTransaction(3, 1000) → "You ordered 3 droids worth 3000 credits!"
makeTransaction(10, 500) → "You ordered 10 droids worth 5000 credits!"
</pre>

<hr/>

<h2>🔹 Task 2: Product Delivery (<code>task-2.js</code>)</h2>
<p>A function that calculates the total delivery cost (product price + delivery fee) and returns a formatted message.</p>

<pre>
function getShippingMessage(country, price, deliveryFee) {
  const totalPrice = price + deliveryFee;
  return `Shipping to ${country} will cost ${totalPrice} credits`;
}
</pre>

<h3>✅ Test Results</h3>
<pre>
getShippingMessage("Australia", 120, 50) → "Shipping to Australia will cost 170 credits"
getShippingMessage("Germany", 80, 20) → "Shipping to Germany will cost 100 credits"
getShippingMessage("Sweden", 100, 20) → "Shipping to Sweden will cost 120 credits"
</pre>

<hr/>

<h2>🔹 Task 3: Element Width (<code>task-3.js</code>)</h2>
<p>A function that calculates the total width of an element (content + padding + border) assuming <code>box-sizing: border-box</code>.</p>

<pre>
function getElementWidth(content, padding, border) {
  return parseFloat(content) + 2 * parseFloat(padding) + 2 * parseFloat(border);
}
</pre>

<h3>✅ Test Results</h3>
<pre>
getElementWidth("50px", "8px", "4px") → 74
getElementWidth("60px", "12px", "8.5px") → 101
getElementWidth("200px", "0px", "0px") → 200
</pre>

<hr/>

<h2>📌 Summary & Reflection</h2>

<p>Great start! 🎉  
In Module 1, you learned the <b>fundamentals of JavaScript</b>:</p>

<ul>
  <li>Declaring and using <b>variables</b></li>
  <li>Working with <b>different data types</b>: numbers, strings</li>
  <li>Basic <b>string operations</b> (concatenation, template strings)</li>
  <li>How to define and call <b>functions</b></li>
  <li>Returning values using <code>return</code></li>
</ul>

<p>This module forms the foundation for everything else. Now, with these basics mastered, you’re ready to move on to more complex topics like branching and loops in Module 2.</p>

<hr/>

<h2>📌 Overview</h2>
<ul>
  <li><b>Task 1:</b> Droid order calculation</li>
  <li><b>Task 2:</b> Shipping cost calculation</li>
  <li><b>Task 3:</b> Element width calculation</li>
</ul>
