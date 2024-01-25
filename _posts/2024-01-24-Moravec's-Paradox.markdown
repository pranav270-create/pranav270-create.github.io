---
layout: post
title:  Moravec’s Paradox and Evolution
description: Why seemingly easy tasks for humans are difficult for robots
date:   2024-01-24 15:01:35 +0300
image:  '/images/moravec_canny.jpeg'
tags:   [reinforcement learning]
---

As a roboticist, I often ponder the nature of automation. The common narrative in science fiction depicts dexterous and intelligent robots, first displacing labor workers until eventully surpassing human conciousness. Reality seems more dull, and occurs in reverse.

Indeed, leafing through dry and lengthy reports from McKinsey will inform you of the gradual automation of ‘soft skill’ white collar jobs. While such forecasts are undoubtedly informed by the tantalizing promises of GPT4, the underlying phenomenon has been known by researchers for decades, just not relevant enough to permeate the global consciousness.

In the 1980s, Hans Moravec, Rodney Brooks, Marvin Minksy, and others coined the term ‘Moravec’s Paradox’ to explain the perplexing gap between software capabilities in reasoning versus sensorimotor skills. As the quote (not so famously) goes:

> It is comparatively easy to make computers exhibit adult level performance on intelligence tests or playing checkers, and difficult or impossible to give them the skills of a one-year-old when it comes to perception and mobility
>
> <cite>Hans Moravec</cite>
>

Indeed, computers first solved problems that humans could not quickly, such as multiplying large numbers or calculating exponentials. They did so by connecting simple, deterministic units of computation into larger, more powerful, systems. This eventually led to symbolic solvers and optimization methods that could tractably determine optimal outcomes for more complex problems like a supply chain. Moore's Law coupled with algorithimic advances then leapfrogged another level, and in 2016 AlphaZero defeated a world champion in Chess and Go. Recently, in 2023, GPT finally proved that even the domain of language can be conquered with adequate data and adequate compute. Put simply,

> the hard problems are easy and the easy problems are hard 
>
> <cite>Stephen Pinker</cite>
>

This becomes even more concrete when we start comparing apples to apples. By measuring the time that a program takes to run, we can understand the complexity of the task at hand (working in energy units may be the most fair metric across compute types but leaving that for another day). Now let us reconsider our list of skills:

* For calculating an exponential, pretty fast. 
* For solving an optimization program, depending on the formulation, reasonably fast, with a need for parallelization.
* For defeating a world champion, some distributed compute involving GPUs, pretty hefty.
* For mastering language, over 1 trillion parameters in one of the largest distributed clusters ever built.

We could stop there. But what is cooler is that we can link the 'computer clock time' to solve a problem to the ‘real clock time’ evolution took to solve it:

* For learning language, the question is up for debate. Laryngeal descent theory argues that we did not have the anatomically requisite parts for modern speech until 200,000 years ago, thereby placing speech with the arrival of modern homo sapiens. A 2019 study in Science Advances calls this into question, arguing that old-world monkeys 27 million years ago also possessed the requisite parts, but needless to say, the modern abstractions of language are a newer phenomenon.

* For learning chess, the first historic estimate of the game places it around 6th century AD during the Gupta dynasty of India, known then as Chaturanga. Other historic evidence places a similar game in Ancient Egypt, with the point being that our ability to reason in such a format can be upper bounded by 5,000 years.

* For learning exponentials and linear solvers, our human hardware has either not adopted that or manifested itself in rare bursts of genius like Srinivasa Ramanujan who could ‘see and hear numbers’. Still, say 500 years.

Notably, time is only half the picture. The other half is Darwin's evolutionary pressure. The more critical a skill is for survival, the stronger the gradient signal is for improving it. To put it in pseudo-mathematical terms, when solving an optimization problem, one must take a starting guess, and then know in which direction to improve that guess. A common method for getting this direction is to use gradients, which tells you the maximal rate of increase, with respect to the objective, for each variable in your problem. However, it is easy to get stuck in a local minima. Hence, another method for getting the direction is to use simulated evolution, which essentially defines mutation operators over a population of candidate solutions, and only retain the ones that are the highest performing (with some caveat for retaining a diverse set of solutions too). This approach is sample inefficient, but can illuminate more of the search space and hence potentially yield globally better solutions.

Given this context, if we frame each of these tasks as an optimization problem, i.e. trying to make humans the best at executing said skill, we can multiply the real clock time needed to develop this skill by the population size undergoing the optimization by the approximate evolutionary pressure for that skill at that point in time. If we then try to back calculate the cost of having a robot learn sensorimotor perception, navigation, and manipulation, making sure to include the population size of *all* species undergoing common evolution before a diverging point in the branch, we get a number that is astronomically higher than all the other tasks.

| Task | Clock Time (Millions of Years) | Population Size (Billions) | Survival Value | Cost |
|:----:|:----------------:|:---------------------------:|:----------------:|:----:|
| Math | 0.0001 | 8 | 0.000001 | Low |
| Chess | 0.005 | 20 | 0.0000001 | Low |
| Language | 0.2 | 30 | 0.1 | Medium |
| Sensorimotor | 300 | 1000 | 1 | High |

Naturally, this has implications for the difficulty of learning a general purpose policy that is as robust as humans-- in my mind, it is possible that we birth conciousness via higher orders of reasoning and thinking before creating a humanoid robot as dexterous and nimble as humans.
