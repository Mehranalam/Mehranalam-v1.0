---
title: How to Write Software With Mathematical Perfection
date: 2023-03-32
description: Modern computers can effectively coordinate with each other because of the work of the computer scientist Leslie Lamport. He’s since turned his attention to making programming itself more efficient.
image: images/Lamport.jpg
tags:
   - Mathematical
   - software 
   - programming
   - technology
---

[eslie Lamport](http://www.lamport.org/)  may not be a household name, but he’s behind a few of them for computer scientists: the typesetting program LaTeX and the work that made cloud infrastructure at Google and Amazon possible. He’s also brought more attention to a handful of problems, giving them distinctive names like the bakery algorithm and the Byzantine Generals Problem. This is no accident. The 81-year-old computer scientist is unusually thoughtful about how people use and think about software.

In 2013, he won the A.M. Turing Award, considered the Nobel Prize of computing, for his work on distributed systems, where multiple components on different networks coordinate to achieve a common objective. Internet searches, cloud computing and artificial intelligence all involve orchestrating legions of powerful computing machines to work together. Of course, this kind of coordination opens you up to more problems.

“A distributed system is one in which the failure of a computer you didn’t even know existed can render your own computer unusable,” Lamport once said.

Among the biggest sources of problems are “concurrent systems,” where multiple computing operations happen during overlapping slices of time, leading to ambiguity: Which computer’s clock is the right one? In a seminal  [1978 paper](https://dl.acm.org/doi/10.1145/359545.359563), Lamport introduced the notion of “causality” to solve this issue, using an insight from special relativity. Two observers may disagree on the order of events, but if one event causes another, that eliminates the ambiguity. And sending or receiving a message can establish causality among multiple processes. Logical clocks — now also called Lamport clocks — provided a standard way to reason about concurrent systems.

With this tool in hand, computer scientists next wondered how they could systematically make these connected computers even bigger, without adding bugs. Lamport came up with an elegant solution: Paxos, a “consensus algorithm” that allows multiple computers to execute complex tasks. Without Paxos and its family of algorithms, modern computing could not exist.

Photo by Talia Herman for Quanta Magazine; video by Emily Buder and Marcos Rocha for Quanta Magazine

In the early 1980s, as he developed the field, Lamport also created LaTeX, a document preparation system that provides sophisticated ways to typeset complex formulas and format scientific documents. LaTeX has become the standard for formatting papers not only in math and computer science but also in most scientific domains.

Lamport’s work since the 1990s has focused on “formal verification,” the use of mathematical proofs to verify the correctness of software and hardware systems. Notably, he created a “specification language” called  [TLA+](https://lamport.azurewebsites.net/tla/tla.html)  (for Temporal Logic of Actions). A software specification is like a blueprint or a recipe for a program; it describes how software should behave on a high level. It’s not always necessary, since coding a simple program is akin to just boiling an egg. But a more complicated task with higher stakes — the coding equivalent of a nine-course banquet — requires more precision. You need to prepare each component of each dish, combine them in a precise way, then serve them to every guest in the correct order. This requires exact recipes and instructions, written in unambiguous and succinct language, but descriptions written in English prose could leave room for misinterpretation. TLA+ employs the precise language of mathematics to prevent bugs and avoid design flaws.

Using your recipe, or specification, as an input, a program called a model checker will check whether the recipe makes sense and works as intended, producing a dish the way the chef wants it. Lamport laments how programmers often cobble together a system before writing a proper specification, whereas chefs would never cater a banquet without first knowing that their recipes will work.

_Quanta_  spoke with Lamport about his work on distributed systems, what’s wrong with computer science education, and how using TLA+ can help programmers build better systems. The interview has been condensed and edited for clarity.

<img src="https://raw.githubusercontent.com/Mehranalam/Mehranalam-v1.0/master/static/images/Lamport_1.jpg" alt="lamport">

## Introduction

### **Let’s start with Paxos, since it’s such an influential algorithm. What made you start working on it in the first place?**

People were building a system with some code, and I had the hunch that what their code was trying to accomplish was impossible. So I decided to try to prove it, and instead came up with an algorithm that the people should have been using for their system.

### **What was wrong with their original algorithm?**

Well, they didn’t have an algorithm, just a bunch of code. Very few programmers think in terms of algorithms. When trying to write a concurrent system, if you just code it without having algorithms, there’s no way that your program is not going to be full of bugs.

 - source of this article : https://www.quantamagazine.org/computing-expert-says-programmers-need-more-math-20220517/