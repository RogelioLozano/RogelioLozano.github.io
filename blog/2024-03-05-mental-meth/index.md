---
slug: Solving-logical-problems
title: Mental methods to solve problems
authors: [rogelio]
tags:  [mental methods]
---

To start smoothly, I'll share ideas I consider important to keep in mind when hunting counterexamples and rapidly discard conjectures that will go nowhere when solving difficult logical-constructive problems. Almost anyone subconsciously does think in two or three of these approaches, but it is useful to have a reminder of these methods of thinking.


- Think small – Start with small examples because they are easier to construct and reason about and allow you to grasp the fundamental ideas that are in the core structure of the problem.

- Think exhaustively – There are usually only a small number of possible instances for the first non-trivial value of n. For example, there are only three distinct ways two intervals on the line can occur: as disjoint intervals, as overlapping intervals, and as properly nesting intervals, one within the other. All cases of three intervals can be systematically constructed by adding a third segment in each possible way to these three instances. 

- Hunt for the weakness – If a proposed algorithm is of the form “always take the biggest” (better known as the greedy algorithm), think about why that might prove to be the wrong thing to do.

- Go for a tie – A devious way to break a greedy heuristic for example is to provide instances where everything is the same size. Suddenly the heuristic has nothing to base its decision on, and perhaps has the freedom to return something suboptimal as the answer.

- Seek extremes – Many counter-examples are mixtures of huge and tiny, left and right, few and many, near and far. It is usually easier to verify or reason about extreme examples than more muddled ones. 

- Divide and conquer - A classical mental model to approach problems that can be divided into subproblems of smaller data size. The resulting structure after applying the method is usually a recursive tree where each node has the subproblem of smaller data size. One classical Example is MergeSort (with a runtime complexity of O(nlog(n)))

