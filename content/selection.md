+++
title = "You care about selection bias because you care about causation"
date = 2023-01-02
description = ""
+++

When I see something criticized for selection bias, it's almost always to caution against making inferences related to causation. In particular, the issue is almost never directly about the sample population being "unrepresentative" of a population you're trying to make inferences about.

Rather, it's about how causation relates to what happens when you condition on a variable (for example, on being in the sample population). Both the magnitude and sign of statistical relationships in a sample population can be determined by the sampling process. This makes even "purely statistical" inference about correlations an absolute minefield under selection bias and more or less impossible without some model of what causes what.

Meanwhile, the question being studied is almost never purely statistical, unconcerned with causation. If all you want to do is make observations and calculate likelihoods, you still have to worry about the causal graph for the reasons above, but at least it makes sense to "just ask questions", as it were. But as soon as you decide to act on your information, or even to tell a story about it, you're almost definitely getting involved with causation.

I'm bringing this up in response to Scott Alexander's recent post [Selection Bias Is A Fact Of Life, Not An Excuse For Rejecting Internet Surveys](https://web.archive.org/web/20230101165439/https://astralcodexten.substack.com/p/selection-bias-is-a-fact-of-life). The thrust of that post is that the damage from selection bias depends on what you're trying to do. If you want first-order statistics, selection bias is "disastrous", and if you want second-order statistics, selection bias is "fine-ish". This is the reverse of how I understand statistics, so I'll quote Alexander:

> Selection bias is disastrous if you’re trying to do something like a poll or census. That is, if you want to know “What percent of Americans own smartphones?” then any selection at all limits your result. ... The same is potentially true about “how many people oppose abortion?” or “what percent of people are color blind?” or anything else trying to find out how common something is in the population. The only good ways to do this are a) use a giant government dataset that literally includes everyone, b) hire a polling company like Gallup which has tried really hard to get a panel that includes the exact right number of Hispanic people and elderly people and homeless people and every other demographic, c) do a lot of statistical adjustments and pray.

This is exactly where it's safest to make adjustments, specifically because you don't have to worry about causation. As long as you can estimate how individual variables are biased, you can make an adjustment to, say, describe a population that has those variables in the correct proportions. It doesn't matter *why* you ended up with an unrepresentative sample. The correction needs a model, but it doesn't have to be causal.

I'm not saying this isn't still often doomed to fail. You might not know how your sample is unrepresentative, or you might have a bad quantitative estimate of the selection bias. But you're on solid ground relative to when you're trying to do the same thing with correlations.

Alexander disagrees, I think:

> Selection bias is fine-ish if you’re trying to do something like test a correlation. Does eating bananas make people smarter because something something potassium? Get a bunch of Psych 101 undergrads, test their IQs, and ask them how many bananas they eat per day (obviously there are many other problems with this study, like establishing causation - let’s ignore those for now). If you find that people who eat more bananas have higher IQ, then fine, that’s a finding. If you’re right about the mechanism (something something potassium), then probably it should generalize to groups other than Psych 101 undergrads. It might not! But it’s okay to publish a paper saying “Study Finds Eating Bananas Raises IQ” with a little asterisk at the bottom saying “like every study ever done, we only tested this in a specific population rather than everyone in the world, and for all we know maybe it isn’t true in other populations, whatever.” If there’s some reason why Psych 101 undergrads are a particularly bad population to test this in, and any other population is better, then you should use a different population. Otherwise, choose your poison.

> Sometimes a correlation will genuinely fail to generalize out of sample. Suppose you find that, in a population of Psych 101 undergrads at a good college, family income is unrelated to obesity. This makes sense; they’re all probably pretty well-off, and they all probably eat at the same college cafeteria. But generalize to the entire US population, and poor people will be more obese, because they can’t afford healthy food / don’t have time to exercise / possible genetic correlations.

This is an odd perspective to me. In particular:

> (obviously there are many other problems with this study, like establishing causation - let’s ignore those for now)

What? That's nearly the whole point! Worrying about selection bias *is for* worrying about causation.{% note() %} And if you don't care about causation, why study the question? I don't care if eating bananas is correlated with IQ, either in the sample or in the general population. When are you in a situation where that's what you want to know? Am I planning to see someone eat a banana and adjust my estimate of how smart they are? I'd be studying the question to understand something about brain function and nutrition, or to decide whether to eat more bananas—knowing the mere correlation in a sample is almost entirely useless without a causal model, even if I don't call it that. {% end %}

But not to fight the hypothetical, let's continue:

> But it’s okay to publish a paper saying “Study Finds Eating Bananas Raises IQ” with a little asterisk at the bottom saying “like every study ever done, we only tested this in a specific population rather than everyone in the world, and for all we know maybe it isn’t true in other populations, whatever.” If there’s some reason why Psych 101 undergrads are a particularly bad population to test this in, and any other population is better, then you should use a different population.

I just said I wouldn't fight the hypothetical, but—it's not okay! Please, absolutely don't do this. "Raises" is a causal word, and that's not what you found.{% note() %} I do appreciate using "Study Finds" rather than "Study Shows", since it's a step closer to a literal description of what happened here. {% end %}

That aside, I'm struggling to understand why trying to generalize about the correlation from this study is any less disastrous than trying to generalize about how many people eat bananas. In the picture Alexander seems to have, conditioning on selection affects correlations in a better-behaved way than it does simple proportions, despite inheriting first-order problems alongside its own unique ones.

I think the disconnect is in what kind of inquiry we're thinking about. If you see some survey numbers, but you don't know anything about the relationship between the sample and the population, then you might be better off just throwing those numbers out. But if you see a correlation, and you don't know anything about the sampling process... no, you want to throw those out even faster. Causal inference is, famously, hard. You're not doing yourself a favor by thinking really hard about it so you can be a good Bayesian and emit a number. What's going on here?

Alexander concludes:

> Selection bias is fatal for polls, but only sometimes a problem for correlations. In real life, worrying about selection bias for correlations looks like thinking really hard about the mechanism, formulating hypotheses about how you expect something to generalize to particular out-of-sample populations, sometimes trying to test those hypotheses, but accepting that you can never test all of them and will have to take a lot of things on priors.

If you like. But even that still sounds *way harder* to me than adjusting proportions. This is territory where following best-effort gun-to-your-head estimates can and often does take you in exactly the wrong direction. If you have a biased sample, you can often write down some bound on how wrong (and in what direction) your proportions are likely to be. This is not so much true of correlations.

Is this a problem for every observational study, not just internet polls and reader surveys? I'll admit I take a relatively hard line on this, but: yes, of course. Even so, they do often at least attempt to be quantitative in how they handle these problems.