---
title: 'Saddle Point'
date: 2021-08-06
permalink: /problems/2021/08/saddle-point/
tags:
  - problem
  - game theory
---

This is a interesting problem in the game theory course.

## Problem

For any matrix without same entry values, prove that there is a saddle point, which means a place which is both a row minimum and a column maximum, where there is a saddle point in every $2$ by $2$ submatrix.

## Sol

Find $A$ with the maximal value among all row minimums.

If there's no saddle points, find its column maximum $B$.

Then consider the new row minimum $C$. We know $C<A$.

Then find $D$ to construct a $2$ by $2$ submatrix.

We can show that $A<B>C<D>A$, which has no saddle point.

Therefore, the statement is true.