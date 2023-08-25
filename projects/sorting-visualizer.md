---
layout: project
type: project
image: img/sorting_visualizer.png
title: "Sorting Visualizer"
date: 2022-01-07
published: true
labels:
  - Algorithms
  - React App
  - Javascript
summary: "A React web app that I developed to visualize the employment of various sorting algorithms on unorganized data."
---

<img class="img-fluid" src="../img/react_app.png">

This sorting algorithm visualizer tool was created to help myself and others visualize how various sorting algorithms worked to sort data in real-time. By being able to visually see each step of the algorithms play out, it helps the user determine the effectivness of these algorithms. Most importantly, it allows the user to visually see how much a particular algorithms solving time scales with input size.

Below is a brief explanation of the capabilities of the app.

<hr>

<pre>
The webpage allows you to select an array size for the unorganized data, adjust the speed of the solver, and choose the sorting algorithm to use. Once you've configured your preferences, you can run the solver, and the sorting algorithm will play out on the unorganized data in real-time. During the visualization, the indices (idx values) in the array that the algorithm is currently focusing on will be highlighted in red. As the algorithm determines that certain indices are in their sorted positions, they will be highlighted in green. The visualizer achieves this by capturing snapshots of the array after each iteration of the selected sorting algorithm. These snapshots are then refreshed on the webpage, allowing you to see the step-by-step progress of the sorting process.

</pre>

<hr>

Source: <a href="https://github.com/matthewtkouchi/sorting-visualizer-tool"><i class="large github icon "></i>matthewtkouchi/sorting-visualizer-tool</a>.
