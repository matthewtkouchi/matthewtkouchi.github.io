---
layout: essay
type: essay
title: "Applications of Sofware Engineering"
# All dates must be YYYY-MM-DD format!
date: 2023-12-13
published: true
labels:
  - Open Source Development
  - Functional Programming
  - Design Patterns
---

# Introduction
After finishing ICS 314 this semester, I really found a new appreciation for dynamic languages and the software principles that come with them. Initially, as a computer engineering major who enjoys more systems-based firmware, I wanted to trudge through the course and be done with it, since I assumed software engineering was more tuned towards mobile and web app development. However, as the semester continued, I found myself quite interested in the lesson plans, and even doing extra readings over the weekends. While the bulk of the coursework was focused on app development, I could definitely see the principles we used being helpful in some of my current works. Throughout the semester, as we learned new topics, I found myself implementing them into my current projects as well as discovering a new understanding to some of the principles I already used. 

# Github Project Management 
One of the most important concept of the course was its emphasis on open-source software development and configuration management. In my undergraduate research project, in the Liquid-Metal Electronics team, documentation is extremely important. Most of the work we do is continued from semester to semester, and often, testbeds for various electronics can be derived from past alumni's work. In this sense, because my graduation is near, I became increasingly interested in an efficient method to document my work. For hands-on work, it was fairly easy to write up documentation and record videos for later students, but for code I worked on, I was originally just uploading the latest versions to a shared Google drive with attached dates. Obviously, this is very inefficient.</br>

Through this course, I learned a great deal on managing my Github projects. Mainly, the project board and branch tips were extremely helpful to me. Essentially, every small change made to the overall project was assigned an issue and a branch dedicated to that issue. All the code to implement that small change is done in a branch with the name of that issue number. I find this very useful for my needs since it reduces the confusion on what code was added for what purpose. This way, I don't have to write so many comments in my code to ensure the future group members can replicate my work. I plan to implement this project management for the remainder of my group's work. 

# Bug Resistant Code
Another helpful software engineering concept taught this semester was functional programming. Functional programming is the art of using functions in software to make the code more maintainable and bug resistant. Mainly, functional programming advocates for the use of pure functions, whose outputs are solely determined by the inputs and the function itself. This way, when bugs occur, they can normally be tracked down to a function, where the errors are localized. Unlike project management, this is something that I already had a fair deal of experience with and strongly support in my style of coding. However, this course definitely improved my skills and taught me the power of higher level languages for this specific purpose. I normally code in lower level languages like C, as it has more room for performance optimization. Javascript has a more dynamic approach and its something I am starting to really appreciate. The combination of functional programming, with high level object abstractions has really started to grow on me this semester. I started to use higher level languages more because of this. For (my radiation pattern testbed), while I probably could make it run faster using C, the time I save using pre-built libraries and functionalizing everything is unmatched. 

# Design Patterns
The final software concept I will talk about in this writing is design patterns. Design patterns are basically repeatable solutions. I also learned about these this semester and it left an impact on the way I think about coding in general, not just for web apps. It's obvious that many problems have similar solutions. That's why there are so many amazing open-source libraries and packages available for all types of applications. People recognized that certain problems are always being run into and they made these libraries to help others that will inevitably end up in the same position. The reason why I found this concept so incredibly helpful is not because of its use in code development, but in the learning process. </br>

Algorithms are very important for my work and to learn them it's a pretty big grind. LeetCode, YouTube videos, blogs. I've done them all. It goes without saying that they are helpful, but once I take a small break, I forget the solutions fairly quickly. When I learned about design patterns this semester I realized that it was the answer to how to retain my knowledge longer. Many problems sound different when you read it for the first time, but if you can recongize the patterns behind the questions, the solutions take on similar forms. This is essentially the whole idea behind design patterns, and I've started to use it when working on interview questions. For example, there are plenty of simple linked list questions in algorithms. A common design pattern between them is the use of two pointers. 
```
1.Detect a Cycle in a Linked List::
- Use two pointers to traverse the list.
- If there is a cycle, the leading pointer will eventually meet the trailing pointer.

2.Find the Middle of a Linked List:
- Use two pointers, one incrementing by one and one incrementing by two.
- When the leading pointer reaches the end, the trailing pointer will be at the middle.

3.Remove Nth Node from End of List:
- Use two pointers, one ahead of the other by N steps.
- Move both pointers until the leading pointer reaches the end.
- Update the next pointer of the node to be removed.
```
In these examples, the questions may not sound like they have any correlation but they do. By understanding the design patterns between these questions, its much easier to remember the solutions. I've been using this concept to remember the structure of a solution rather than the individual answer to an individual problem. 

# Conclusion
In conclusion, the software engineering concepts I learned this semester completely changed my opinion on the course. I initially thought it was going to be all about HTML and making apps, but the underlying teachings are something that I will carry with me for the remainder of my career.


