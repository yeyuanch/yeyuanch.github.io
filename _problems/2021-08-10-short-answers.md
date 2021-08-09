---
title: 'Short answers for the puzzle TOAD'
date: 2021-08-10
permalink: /problems/2021/10/short-ans/
tags:
  - problem
---

These are short answers (and my ideas when trying to work out the problems) for the problems in [Puzzle Toad](https://www.cs.cmu.edu/puzzle/).

\"*" means fun in the list. "U" means I didn't finish writing the solution.

## Problem 39

We find $L$ with dishes one by one. At one round, we can compare any two dishes. When more than a half prefers one dish, then it beats the other. We can find one dish beats at least a half of other dishes. We add this in $L$ and delete this and the dishes $d$ beaten by it. Now recursively do this, by $1024=2^{10}$, we can terminate in $\| L \| \le 10$.

## Problem 38 (Expectation, *)

The problem is interesting! First we let the saucers on a triangular grid, then with calculation we can get the area of the saucers is $(3\pi/4) / (3\sqrt{3}/2) = \pi/2\sqrt{3} > 0.9$. Now we move the grid, by linearity we know the expected points to be covered is $10\pi/2\sqrt{3} > 9$, so we know it must be possible to achieve $10$.

## Problem 37 (*)

Do things by this algorithm in one turn (with length $n$, $n$ is the worm's length): 

- If no $0 \rightarrow 1$, we perform $1 \rightarrow 0$.
- If at least once $0 \rightarrow 1$, we perform $1 \rightarrow 1$.

Then in every turn, it will become $0$ or the binary number will increase.

So at last we can get the worm $0...0$.

## Problem 36 (IMO2011, hard, *)

The point is: in the whole procedure, the number of points on the left or right remains the same (exclude the pivot), which can be proved by imagining one turn of pivot changing.

Now consider a general coordinate with every two points differ in both $x$ and $y$. We let the line to be on $+y$ direction, rotating clockwise from the point whose $x$ coordinate is the $\lfloor n/2 \rfloor - th$ smallest. Then after it rotating $\pi$, we can find what's the pivot by above!

Then the fact is, for any point, it may be the starting or ending pivot, or it may cross the line, which requires it to be a pivot at some time. Therefore, we know every point is struck down. 

## Problem 35 (hard, U)

## Problem 34

The problem is equivalent to: for odd $n$, show that in $F_2$, symmetric matrices with diagonal entries $0$ are singular. We may calculate the determinant to prove this (not trivial).

## Problem 33 (easy)

A easy probability problem. First assume they are just on the side of the circle, and one is on angle $0$, then draw a square area to represent the other two angles and discuss the area for them to contain the center. It is easy to get that every turn the probability is $1/4$, then just deal with the expectation.

## Problem 32 (*)

An interesting construction problem. A simple approach is $1\ 1\ 1\ 1\ 1\ 1$ $\rightarrow$ $3\ 0\ 3\ 1\ 1$ $\rightarrow$ $12\ 0\ 1\ 1$ $\rightarrow$ $2048\ 0\ 1$ $\rightarrow$ $2^{2048}$. The solution find that sometimes using button $A$ is better and gives a better answer: $3\ 0\ 3\ 1\ 1$ $\rightarrow$ $14\ 0\ 1\ 1$ $\rightarrow$ $20480\ 0\ 1$ $\rightarrow$ $5 \times 2^{20479}$. Of course we should buy this, do the operation and find that this is much better than a lottery.

## Problem 31 (easy)

**(a)** The first player delete 50 first, then every turn he maintains the amount of two sides of $50$ to be the same by deleting numbers from inner to outer. Then the last two are on different sides of $50$. He delete $54$ numbers, so the gap is at least $55$.

**(b)** The first player delete $2$ and now we see it as $5$ $1,2,3,4,5$s with an extra $1$. Now make it into pairs $(1+4),(2+3)$, then the first player can delete the number in the same pair after the second player. Then there remains an $1$ and 5 $5$s. The player can delete $1$ first after any deletion of $5$ or delete a $5$ after the deletion of $1$. Then the remain numbers form a pair or are two $5$s.

## Problem 30 (hard, U)

## Problem 29

Of course we can induction to get the conclusion, but informally we can think this: the answer will be yes if someone goes to the last person's seat, and the answer will be no if someone goes to seat 17. The probabilities must be the same in any random move. Then the answer is $1/2$.

## Problem 28 (*)

A short and beautiful proof is given by solution. Consider $n$ walkers, for the edges with $1,2,...,m$, swap the walkers on the edge in turn. Then after $m$ turns the $n$ walkers walks $2m$ in total, which shows that at least one walks with distance $2m/n$.

## Problem 27 (easy)

$n$ people guess the sum to be odd, while other $n$ guess the sum to be even. 

It is a technique to make local guesses related to global situations to give a win probability. A more complex example is about the permutation, which is also a classical problem.

## Problem 26

First guess where they are: one shop is likely to be placed on the center by symmetry. The other $6$ then can each cover a $60$ degree part of the circle. By calculation we can find that the radius can be $1/2$ when we place the shops on the midpoints of endpoints of the $60$ degree arcs.

To prove the optimality we consider the circumference. A circle with radius < $1/2$ cannot cover a $60$ degree arc, so we need $7$ cycles all intersect the circumference. But in this case, the center is not covered.

## Problem 25

If yes, WLOG we can suppose the period is a multiple of $100$, so we can suppose the sequence is started from $f(0)=0$. We soon find that $f(i)$ is the parity of number of $1$s in the binary expansion of $i$. Then if for $i \geq 2^k$ there's a period $t=1...$ with $p$ digits, $p<<k$. We consider two $k$-digit numbers $10...0$ and $10...010...0$ with the last $p$ digits $10...0$, then it's easy to see there's a contrast. The official solution gives a stronger conclusion.

## Problem 24 (*)