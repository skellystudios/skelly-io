---
layout: post
title:  "A crossword fit for a wedding"
date:   2016-02-12 07:39:51 +0000
categories: technology
sidebar-image: https://images.unsplash.com/photo-1447069387593-a5de0862481e?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&s=0dab06e522cf4cd96ee75e9801e73c8a
photo-credit: "Joanna Kosinska - www.joannakosinska.com"
hide: true
---

# Fitting a good cryptic crossword grid

***

Some friends of mine recently got married, and sent a crossword along with their wedding invitation (although solving it wasn't required for a successful RSVP). I happened to ask him how he put the grid together.

It turns out that it's surprisingly hard to put together a good grid. It's even harder to do it while you're also planning a wedding – in the end the friend just did a sort of monte-carlo simulator, effectively throwing words down until they landed on a the grid in a legal way. He ran that on his laptop (specs unknown) for a week and then selected the best solution

## What the problem is (and isn't)
- Given a list of words, fit all (or most) of them onto a grid
- **Isn't**: Fitting a much larger list of words onto a grid of standard form
- **Isn't**: Randomly generating whole crosswords using the above technique


## What constitutes a good solution

- Fitting to a normal grid
- Symmetry
- Denseness
- Smallest possible grid size
- Number of intersections (checked letters)

# Challenges

- Spacial representation required (?) – I.e. can't just represent as a graph (or can you?)
    - Hard to find a good representation for it at all!
- Massive problem space
- Is is possible to determine a correct solution
- Solution to sub-problem not necessarily on the route to the solution to the real problem – adding an extra word can completely change the solution space
- Not always solvable, for very degenerate cases
- Fitness criteria not well defined

## Approaches

### Monte carlo

**Outline**
Throw down items until they "stick", keep grids that are better than others

### Genetic algorithm

**Outline**

- Create a fitness function that determines the "quality" of a given grid.
- Create a way of mutating a grid (i.e. throwing down an available word, or translating the position of an existing word)
- Continute until grids

Local maxima may be found


### Memoization with DFS

**Outline**
Create various sub-trees and stick them together.

- How to find an algorithm to work out where two subtrees can be stuck together

Should find the optimal solution eventually – but the state space is huge

### Satisfaction constraint solver








***
***
***

# Ideas to write about
- Weddings: invitiations, and clever schemes around them
