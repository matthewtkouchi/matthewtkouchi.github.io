---
layout: project
type: project
image: img/automation.jpg
title: "Radiation Pattern Testbed Automation"
date: 2023-02-14
published: true
labels:
  - Virtual Interface
  - SCPI
  - GPIB
  - PyVisa
summary: "A quick set of scripts I created to automate the manual testbed the UH Manoa liquid-metal electronics group was utilizing."
---

A radiation pattern test is a common test in wireless propagation tests, for example, using antennas, reflect arrays, etc. 
The radiation pattern of a Device Under Test (DUT) is the gain or received power across some angular range around the DUT.
For example, every antenna has a 360 degree radiation pattern measurement done to quantify how directive it is, and the efficiency of it.
An example radiation pattern is shown here (source:https://www.sciencedirect.com/topics/engineering/radiation-pattern):

<img class="img-fluid" src="../img/antenna_rad.jpg">
<hr>
To automate this type of test on the current testbed of the liquid-metal electronics group, I created a few scripts that use PyVisa to communicate with various 
programmable interfaces of the hardware equipment. For example, the motion controller we used to move the antenna 180 degrees in the azimuth direction is controlled
using a GPIB interface, which is made possible using Serial.

Hers a GPIB connector: <br>
<img class="img-fluid" src="../img/gpib.jpg">
<hr>
The current implementation of the automation scripts are made especially for the equipment in the POST 427 labratory. In the future I plan to add a front-end interface using tkinter to improve the quality-of-life of the application.
<hr>
Source: <a href="https://github.com/matthewtkouchi/automated_test_bed"><i class="large github icon "></i>matthewtkouchi/testbed-automation</a>.
