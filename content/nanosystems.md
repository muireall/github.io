+++
title = "Atomically precise manufacturing in principle"
date = 2023-01-15
description = "Not mere difficulty: challenging relevance to longtermism and AI risk"
+++

In the 1992 book *Nanosystems*, K. Eric Drexler sketched some bounds on maximum capabilities of nanotechnology under classical physics and chemistry, alongside proposals for realizing those capabilities. The resulting picture of atomically precise manufacturing (APM){% note() %} You may encounter overlapping terms, like molecular nanotechnology (MNT), positional chemistry, or mechanosynthesis. The term "nanotechnology" on its own refers to something else in the modern scientific community.{% end %} purports to comprise a set of components and systems, inspired by mechanical engineering, with transformative capabilities within the bounds of physical law.

Scientists who encounter these ideas have some common intuitive objections:

- Nanoscale devices are made up almost entirely of surfaces and edges, which can behave remarkably differently from bulk materials of the same composition. This, generously, presents a wide range of problems for design of components like those presented in *Nanosystems*.
- Drexler's simulated molecules look nothing like the molecules typically studied by those simulation tools, to the extent that it's not clear that the results have any valid intepretation. There are likely to be nearby lower-energy configurations of the proposed final products, and a synthesis pathway of stable intermediate products is not remotely guaranteed.
- More broadly, the analysis is unsystematic and nonstandard, and even if correct is certain to be missing many important considerations.
- Error-free operation or error correction (perfect yield or perfect purification) seems necessary to get useful throughput as you synthesize products requiring more processing steps.
- Absolutely precise control of position and energy seems necessary to avoid errors.
- Ultra-high-vacuum operation seems necessary to eliminate uncontrolled adsorption of unwanted species on surfaces.
- Cryogenic operation seems necessary to avoid control being overwhelmed by thermal fluctuations and Brownian motion.
- Slow speeds seem necessary to avoid overheating, particularly without solvent flow to carry away heat.
- There's not enough room for fan-in of precise positional controllers for all degrees of freedom ("fat fingers").
- There's not enough control of binding energies to precisely release proposed reagents onto a workpiece ("sticky fingers").
- A broad range of chemistry conducted by a fixed set of components seems further implausible. (For example, even if many different molecules can bind to one site, they'll be unequally "sticky".)

But these sorts of concerns don't get at the core of why APM might matter to Effective Altruists, longtermists, and people thinking about global catastrophic risks.{% note() %} For example, see [Nick Beckstead's "shallow investigation" for Open Philanthropy](https://www.openphilanthropy.org/research/atomically-precise-manufacturing/). {% end %} Of course these things are *hard*, but if they're speculating about the far-distant future or the capabilities of a superintelligence, mere difficulty may not dominate other considerations. To the extent there's a scientific question they're interested in, it's closer to one of in-principle feasibility than to a specific research program.

So the response from Drexler and others tends to be: yes, these objections all point to obstacles to be overcome. But a ribosome can already assemble long proteins. Of course arbitrary methods aren't guaranteed to work, but that doesn't remotely rule out feasibility.

One sometimes even hears the claim that the particular mechanisms sketched by Drexler are proof of feasibility, providing a *lower* bound on capabilities. This claim, at least, is not defensible. Still, for most purposes, it can be substituted with the claim that his sketch is sufficiently suggestive of something in that ballpark being feasible. I'd like to at least convince you that it's not so suggestive, and maybe point to some tighter upper bounds.

#### Where are all the refutations?

The conversation often derails around here, since this sort of in-principle feasibility is irrelevant to most scientists, who, rather than argue stricter physical bounds, point to the difficulty of particular obstacles, to gaps in the particular models in *Nanosystems*, or to the absence of a plausible research program to get to there from here.{% note() %} Another common derailment is discussion of the ribosome as an analogy or proof of existence for molecular assemblers. For example, one might observe that a ribosome works with a famously small, fixed set of building blocks (amino acids) and even then must be embedded in a ["proteostasis network"](https://pure.mpg.de/rest/items/item_2316631/component/file_2316629/content) involving hundreds of components (over 1,000 in mammalian cells, with some redundancy), including molecular chaperones to assist protein folding and repair and an autophagy system to remove dysfunctional products. This discussion is helpful for understanding some challenges involved, but again, doesn't address in-principle feasibility. {% end %}

To my knowledge, there are no detailed technical objections to Drexler's proposal in print that meet this in-principle bar. Famously, Nobel Prize–winning chemist Richard Smalley [exchanged open letters](https://en.wikipedia.org/wiki/Drexler%E2%80%93Smalley_debate_on_molecular_nanotechnology) with Drexler in the early 2000s, but didn't make arguments more rigorous than any you might see in, well, a blog post. He didn't show that any of Drexler's calculations were wrong, that any proposed structures would fail, or that his concerns were universal, inevitable obstacles to molecular nanotechnology. Smalley's observations are serious and insightful, but as formulated aren't so relevant to arguments that operate on upper bounds.

Would we expect to find such objections in print if APM weren't feasible?

Scientists can convince themselves that Drexler's sketch is infeasible (not merely irrelevant) more easily than one might think from journal articles alone. Once they're sufficiently convinced, there's little reason to pursue the subject further, let alone publish on it. It's of little intrinsic scientific interest to argue an at-best marginal, at-worst pseudoscientific question. It has nothing to offer their own research program or their career. Smalley's participation in the debate certainly didn't redound to his reputation. So there's not much publication-quality work contesting *Nanosystems* or establishing tighter upper bounds on maximum capabilities. But that's at least in part because such work is self-disincentivizing.

Presumably some arguments people find sufficient for themselves wouldn't go through in generality or can't be formalized enough to satisfy a demand for a physical impossibility proof, but I wouldn't put much weight on the apparent lack of rebuttals.

#### Nanotechnology and superintelligence

The most abruptly catastrophic scenarios involving artificial intelligence invoke something like molecular nanotechnology. For example, Eliezer Yudkowsky recently [wrote](https://forum.effectivealtruism.org/posts/zzFbZyGP6iz8jLe9n/agi-ruin-a-list-of-lethalities):{% note() %} Emphasis is as in the original. {% end %}

 > **A cognitive system with sufficiently high cognitive powers, given any medium-bandwidth channel of causal influence, will not find it difficult to bootstrap to overpowering capabilities independent of human infrastructure.**  The concrete example I usually use here is nanotech, because there's been pretty detailed analysis of what definitely look like physically attainable lower bounds on what should be possible with nanotech, and those lower bounds are sufficient to carry the point.  My lower-bound model of "how a sufficiently powerful intelligence would kill everyone, if it didn't want to not do that" is that it gets access to the Internet, emails some DNA sequences to any of the many many online firms that will take a DNA sequence in the email and ship you back proteins, and bribes/persuades some human who has no idea they're dealing with an AGI to mix proteins in a beaker, which then form a first-stage nanofactory which can build the actual nanomachinery.  (Back when I was first deploying this visualization, the wise-sounding critics said "Ah, but how do you know even a superintelligence could solve the protein folding problem, if it didn't already have planet-sized supercomputers?" but one hears less of this after the advent of AlphaFold 2, for some odd reason.)  The nanomachinery builds diamondoid bacteria, that replicate with solar power and atmospheric CHON, maybe aggregate into some miniature rockets or jets so they can ride the jetstream to spread across the Earth's atmosphere, get into human bloodstreams and hide, strike on a timer.  **Losing a conflict with a high-powered cognitive system looks at least as deadly as "everybody on the face of the Earth suddenly falls over dead within the same second".**

Yudkowsky, I believe, has more extreme views on AI "takeoff speed" than most in the community, and many don't see molecular nanotechnology as necessary for AI to be an existential risk. Compare to [Paul Christiano](https://www.lesswrong.com/posts/CoZhXrhpQxpy9xw9y/where-i-agree-and-disagree-with-eliezer):

> By the time we have AI systems that can overpower humans decisively with nanotech, we have other AI systems that will either kill humans in more boring ways or else radically advanced the state of human R&D.

And [Holden Karnofsky](https://forum.effectivealtruism.org/posts/6LTh4foNuC3NdtmZH/ai-could-defeat-all-of-us-combined):

> I think we still have a problem even if we assume that AIs will basically have similar capabilities to humans, and not be fundamentally or drastically more intelligent or capable.

Still, I can see some limited value in directly addressing questions of feasibility.

#### Feasibility arguments

Taking the analysis in *Nanosystems* on its own terms, one can find tighter upper bounds for capability consistent with physics and for performance of the systems proposed as a "lower bound". I wouldn't really encourage anyone to spend time on this, but here are the threads I would pull on:{% note() %} Someone with a background in chemistry or biology would likely find a different set of threads. {% end %}

- *Nanosystems* mainly considers mechanical properties of isolated components and their interfaces. It might be more appropriate to think in terms of collective motion of the whole assembly. For example, stiff six-axis control doesn't help much if the workpiece has levered fluctuations relative to the assembler arm.
- Similarly, in collective motion, non-bonded interfaces are large contributors to acoustic radiation and dissipation, including, for example, interaction of phonons with the thermal strain field. Drexler admits phonon-phonon scattering at interfaces could use more investigation, but he believes their contribution is small, which is odd. It may help to think of an assembly as a solid with low stiffness and highly anharmonic inter-"atom" potentials.
- Edges are important and often dominant in nanoscale friction. Their contribution is hard to quantify *ab initio* and omitted entirely by *Nanosystems*.
- I can't figure out what's going on with the power dissipation calculations.
    - The analysis of energy dissipation in sleeve bearings{% note() %} Section 10.4.6 {% end %} is full of statements that are dimensionally inconsistent (Eqns. 10.19–10.27), and none of the things Drexler could plausibly have meant give his numbers.{% note() %} Sometimes you encounter "engineering formulas" that do not include units, with the implication that you must input values in the units it was written for. If that was the intention here, the engineering formula was not correctly derived. {% end %} If I try to apply his calculations from the beginning, I get a power dissipation that's about two orders of magnitude larger.
    - I'm actually not too concerned about this, not least since I expect these methods are not correct or complete to begin with. As far as I can tell, Drexler's methods and terminology (for example, "band-flutter scattering") originate with him and are not used outside of this text.
    - Most experimental and simulated sliding and rotation of multi-walled carbon nanotubes finds friction higher by orders of magnitude. The most favorable simulation results in the high-speed limit are not terribly far off if you translate things into less idiosyncratic terms, but in that case edge contributions to friction will dominate anyway.{% note() %}Also, proposed operating rotation rates are slower than the thermal rotation rate at room temperature, which seems impractical. {% end %}
- Drexler considers thermal fluctuations very narrowly.
    - For example, *Nanosystems* describes logic rods in a nanomechanical computer (12.3) moving with kinetic energy on the order of their thermal energy. The only error that Drexler calculates—basically, from thermal fluctuations in the rod's extensional degree of freedom—produces a "conservative" error rate of {% katex() %}  10^{-64} {% end %} per logic-rod motion.
    - It might be more appropriate to use fluctuation-dissipation relations to calculate the probability that random forces push the rod beyond the error threshold displacement during a cycle. On the back of the envelope, it seems about as likely as not for the example parameters. This is even before considering that dissipation is likely orders of magnitude too low.

- I don't recall any discussion of torsional rigidity of components. I think you can get a couple orders of magnitude over flagellar motors with CNTs, but you run into trouble beyond that. Demands on torque are surprisingly high.

#### Limits of pure theory

Another line of argument for skepticism about Yudkowsky's "lower bound" scenario is the difficulty of inventing nanotechnology without many sequential rounds of experimental feedback:

- Current *ab initio* simulation methods are accurate only to within a few percent on "easy" properties like electric dipole moments. What tolerances do you need to make reliable mechanisms? Chemically selective mechanisms?
- Nanoscale systems are sensitive to things that are hard to simulate.
    - Chemistry requires a description of electronic degrees of freedom, either from empirical data or from quantum methods. Quantum methods are expensive and become classically intractable for large enough problems. It's generally believed that this is fundamental.
    - Because edges, surfaces, and interfaces are so important, it's often hard to make simplifications from the full system. One example, mentioned above, is friction. Another is surface piezoelectricity and flexoelectricity.{% note() %}Material boundaries lack inversion symmetry, so even centrosymmetric crystals can have surface piezoelectricity comparable to industrial workhorse bulk piezolelectrics. Flexoelectricity—where inversion symmetry is broken due to nonuniform strain—also becomes important at the nanoscale. These are not only a channel for unwanted electrical interactions but also constitute an effective modification of bulk mechanical properties like a beam's bending moment or torsional rigidity. Sometimes in a favorable direction! But it's not clear how accurate simulations are, and it's hard to set up experiments. {% end %} [Surface reconstruction](https://en.wikipedia.org/wiki/Surface_reconstruction) is sensitive to adsorbed atoms. Atoms at bonded interfaces between stable bulk solids can diffuse to form a mixed interface layer. Simulating isolated components is likely not enough.

- I don't expect machine learning to help much, since the kinds of structures in question are very far out of domain, and simulation has its intrinsic hardness problems. Simulating molecules isn't even enough—you need to solve the inverse problem of design, for every set of components and their synthesis pathways.

These are sort of like the original objections in that they don't really address upper bounds or in-principle feasibility. But quantum simulation of large systems is hard even for a hypothetical superintelligence, and there's every reason to expect that that's exactly what's required to get an accurate description of these systems without experimental feedback. (Not to say we even know how to do the relevant experiments.)

#### Apology

Above, I allude to calculations I've done, but I haven't written them down. It's bad form, but I've already given this subject more attention than I can honestly justify to myself. You can tweet at me about it.

This is still more of a notebook entry than a rebuttal. I'm not sure it really accomplishes what I set out to do, but maybe it points well enough to how I might go about it.