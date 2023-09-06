---
layout: essay
type: essay
title: "Asking Smart Questions"
# All dates must be YYYY-MM-DD format!
date: 2023-09-05
published: true
labels:
  - Smart Questions
  - Answers
  - StackOverflow
---

<img class="rounded float-start pe-4" src="../img/dumb-questions.png", alt="Source: haarpia (2013). Word Press. Retrieved from https://haarpia.wordpress.com/tag/bart-simpson/">
## Stop Asking Dumb Questions
Everyones heard the phrase, "There's no such things as a stupid question", but I can tell you from experience that this is a straight up lie. We've all probably been on the receiving end of one, and even more likely, have asked a ton of them. As a student that will soon be transitioning into industry, I find it increasingly important to break the habit of asking dumb questions, and so should you. Rarely does a dumb question result in useful answers, if it dictates an answer at all. It is imparative to learn how to recognize and dumb question and to stop yourself before asking it. Constructing a smart question may seem like a lot of effort, but it is neccesary to efficiently maximize the amount of information you can garner from people more knowledgable and less tolerable than you.

## What Constitutes a Smart Question
A smart question is one that is both specific and measurable. The subject header of a smart question should describe the exact problem that the author is facing. One should be able to read the header and immediately recognize the problem at hand in order to decide if it is their area of expertise. In addition, the question itself must be written in a clear and concise manner. The question does not have to be long, but it should be detailed enough that there is no question in the readers mind about what is wrong, what has been tried, and what the goals of the author are. In this sense, the format of the question should roughly follow the following template:<br>

  1. Describe the problem clearly
  2. Describe the environment it occurs in and the name of any software or hardware frameworks being used in the project
  3. Describe previous reasearch and attempts at solving the problem
  4. Mention any recent software configuration changes (e.g. versions or udpates)
<br>

Finally, at the end of each smart question, a quantifiable goal should be mentioned to the reader. What do you want the solution you get to accomplish? Don't just ask someone to "fix it", unless you want an empty inbox. Do you need the solution to be concise? Do you need it to be cross-platform compatabile? Make a specific and measurable goal.

# Stack Overflow Examples
Stack Overflow is the hub for programming questions for anyone having issues with their code, or people that simply want to learn more about coding. Using this populated forum, I found an example of a good and not so good question to be studied. 

<a href="https://stackoverflow.com/questions/76860140/convenient-way-to-declare-2d-or-even-higher-dimension-arrays-with-stdarray">the following example</a> is of a good and smart question. It exhibits all the properties of a question that will be received openly and that will garner quality responses. 
```
Q: Convenient way to declare 2D (or even higher dimension) arrays with std::array

I'm about to convert a lot of old C++ code to more modern C++.

There are many raw 2D arrays in that code like:

Foo bar[XSIZE][YSIZE];

And I'm about to replace these declarations with

std::array<std::array<Foo, YSIZE>, XSIZE> bar;
This is a convenient way because the statements stay the same and the code is supposed to behave the same as with raw arrays with the additional benefit of being able to have out of bounds checks in debug builds.

But IMO the std::array<std::array<Foo, YSIZE>> is somewhat cumbersome and not easy to read, and with 3D arrays (although I have none) it would even be worse.

Right now I'm using this macro to make the declaration more readable:

#define DECLARE_2D_ARRAY(type, x, y) std::array<std::array<type, y>, x>
DECLARE_2D_ARRAY(Foo, XSIZE, YSIZE) bar;

But I feel this to be a macro hack, and I'm wondering if there is a cleaner, more C++ way to do something similar.
```
The author of this question conveys exactly what he is trying to do, what problem he is facing, what methods he has tried, the shortcomings of those methods, and what his goal for possible solutions is. In other words, even though the question is short and concise, its wording is well thought out and intentional. The author shows that he has put some thought into his question and into the solution before he's asked others to provide answers. 

Since the question is simple, but still well worded, the author easily received multiple high quality answers. The answers include explanations of the methods they used, and sample code for implementing sed methods. For example, the top upvoted reply was a very elegant answer that utilized something the author had never heard of before, type alias templates.

```
You can use a type alias template:

#include <array> 
#include <cstddef>

template <class T, std::size_t x, std::size_t y>
using Array2D = std::array<std::array<T, y>, x>;

int main() {
    Array2D<int, 5, 3> arr;
}
You can also generalize it like so for any dimension:

#include <array>
#include <cstddef>

template <class T, std::size_t size, std::size_t... sizes>
struct ArrayHelper {
    using type = std::array<typename ArrayHelper<T, sizes...>::type, size>;
};

template <class T, std::size_t size>
struct ArrayHelper<T, size> {
    using type = std::array<T, size>;
};

template <class T, std::size_t... sizes>
using Array = typename ArrayHelper<T, sizes...>::type;

int main() { 
    Array<int, 5, 3, 4, 3> arr; 
}
```

If a bad question is asked, it will be very rare to receive such nice replies. Take for example <a href="https://stackoverflow.com/questions/15442956/how-to-insert-one-string-into-the-middle-of-another-string">the following Stack Overflow question:</a>

```
Q: How to insert one string into the middle of another string?
I am trying to stick one string into the middle of another string, ex:

String One = "MonkeyPony";
String Two = "Monkey";
How would I put String Two into String One so it would read something like MonkeMonkeyyPony?

What I'm trying to do is insert "Monkey" into the middle of "MonkeyPony" numerous times, so on the first time it would read "MonkeMonkeyyPony", and on the second time it would read "MonkeMonMonkeykeyyPony", etc.

```
I was unable to find much poorly written questions without answers, so instead I present a bad mannered question instead. The header is actually okay since the question itself is relatively simple. The question isn't the most effortful, since it doesn't mention any previous attemps, but is nonetheless readable. The question is simple so anyone can read it and understand what the author wants. The main problem with this question is that it is a duplicate which is taboo in these types of forums. 

Whenever a question is asked, the first thing one should do, is look it up. Manuals, Google, and forums hold the answers to most questions you can think of. Only when it gets very specialized, there is a chance it hasn't been asked before. 

So while this question wasn't inherently poorly written, it still received a multitude of downvotes and stern comments because of the lack of effort taken to verify that it was a duplicate question. If you don't want your inquiries to be met with hostility such as this, write smart questions!

<img class="rounded float-start pe-4" src="../img/downvote.png">


