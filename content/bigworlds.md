+++
title = "Big worlds are hard to keep safe"
date = 2022-09-23
description = ""
+++

A [recent post by Thomaaas](https://forum.effectivealtruism.org/posts/zLZMsthcqfmv5J6Ev/the-discount-rate-is-not-zero) on the EA Forum describes some reasons that the risk of existential catastrophe might not go zero (or down!) in the future.  I wanted to mention one other reason, which is that big worlds are hard to keep safe. For example, if catastrophe can be triggered by unilateral action in a growing population, risk naturally grows over time. That's all. Everything below is just color.

As I wrote [before](../repugnant):

> Context: I'm not a utilitarian. 

> This isn't why I'm not a utilitarian—it's just me playing with some perennial debates reappearing alongside [Michael Nielsen's notes](https://michaelnotebook.com/eanotes/), [requests for critical writing](https://forum.effectivealtruism.org/posts/8hvmvrgcxJJ2pYR4X/announcing-a-contest-ea-criticism-and-red-teaming) on Effective Altruism, and [prompts](https://www.openphilanthropy.org/blog/cause-exploration-prizes) from Open Philanthropy. I do think utilitarians (and I'm in particular thinking of longtermist Effective Altruists) should take standard objections more seriously and be more self-skeptical in their reasoning. (I'm also not an Effective Altruist, although I support GiveWell.) This has all probably been said before.

Here's a toy model. For every billion people, there's a laboratory with a 1 in 1,000 chance per century of an escaped pathogen causing a civilization-ending pandemic. If we have 10 billion people, these labs contribute about a 1% chance of a such a pandemic this century. If we had 100 times that population, 1 trillion people, that chance would be {% katex() %} 1 - 0.999^{1000} ≈ 63\\%.{% end %} If we wanted the same escape risk, we'd have to reduce the risk per lab by about a factor of 100.{% note() %} One trillion people is the "small" future population Thomaaas's argument implies we should worry about, as opposed to, say,  [10^46 future people we could miss out on per century of delayed galactic colonization](https://nickbostrom.com/astronomical/waste). {% end %}

Not all risks are like this. Asteroid impacts will happen at the same rate no matter how many people are on the planet.

Risks that follow combinatorial (rather than unilateral) failure may start smaller but grow even faster. If we have one state with nuclear capabilities per billion people, and a 1 in 1,000,000 chance per century of any pair of nuclear states engaging in a civilization-ending nuclear conflict, then with 10 billion people, then the chance of such an event between any of the 45 pairs of states is about {% katex() %} 45~\times~10^{-6}.{% end %} If we had 1 trillion people and 1,000 nuclear states, then we have 499,500 pairs and a risk of about 39% per century of that level of conflict. We'd have to decrease risk by about a factor of 10,000
per pair to keep the risk about the same with 100 times the population.

We might expect a given pathogen to be less likely to end larger civilizations. Larger population size doesn't give us a well-scaling safety margin against uncontrolled exponential spread, but at least the number of naturally immune survivors should grow with population. The number of survivors might be the difference between being able to restart civilization or not. So maybe we get some reduction of risk of existential catastrophe per escape event for free with the extra population, all else equal. The balance in the toy model depends on the distribution of pathogen lethality and on the survivor-count-dependence of recovery in the aftermath. Similarly, whether a nuclear exchange leads to the collapse of civilization may also depend on population size in a way that's difficult to model.

In general, as the world grows, more things can happen. It's not hard to imagine combinatorial growth in the number of "possible next centuries" as you add more people. Can we keep up and keep risk constant? What does it cost?

In my example from [my previous post](../repugnant) I used a cost to eliminate a fixed risk (in percentage points per unit time) that grew in proportion to the population, calling this "uniform policing". But we really need increasingly strict policing to keep the overall risk constant. For some risks, and in particular those that will come to dominate in large worlds, one needs to multiply by another factor proportional to population (escaped-pathogen-like risk), that factor squared (war-like risk), or even an exponential or factorial in population (risk from dark corners of the full combinatorial space of events).