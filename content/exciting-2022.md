+++
title = "Some things I'm excited about, 2022"
date = 2022-01-22
description = "egg, Julia, space, search, squares"
+++

I may continue to update this list, since these are just the first few things that came to mind. There's nothing necessarily specific to 2022 here other than that I'm thinking about them now and there'll be something to see in the relatively short term.

<!-- more -->

## [egg](https://egraphs-good.github.io/)
The `egg` project is probably the most exciting thing I've seen in computing in the past year. It's an extensible implementation of equality graphs (e-graphs, an efficient representation of equivalence classes of expressions) with fast equality saturation (building the full graph of equivalence classes by applying rewriting rules until a fixed point is reached), in Rust. The idea isn't new—researchers have implemented compiler optimizations this way, generating a large set of equivalent programs and picking the best. But these implementations have been tied to automated theorem provers (which aren't built for fast equality saturation) with ad-hoc extensions for analyzing those programs. In `egg` we have a single implementation specialized for equality-saturation workloads that can be cleanly extended with different analyses. The [paper](https://arxiv.org/abs/2004.03082) introducing it is pretty readable. There are already some varied examples putting `egg` to use (for example, [Ruler](https://dl.acm.org/doi/pdf/10.1145/3485496)), but I think we've barely begun to see what we can do with it.

## [Julia Symbolics](https://symbolics.juliasymbolics.org/dev/)
I'm closely watching the development of the Symbolics ecosystem. (One part of that happens to be the e-graph rewriting backend [Metatheory.jl](https://github.com/JuliaSymbolics/Metatheory.jl) modeled after `egg`.) The home page calls it a Computer Algebra System, but right now developers seem more focused on symbolic-numeric computation. It's in an odd situation where it has trouble simplifying arithmetic expressions with nested subtraction and division, but it can dramatically accelerate differential equation solvers. I think the potential here is underappreciated in scientific computing.

A couple honorable mentions in Julia are the coming generations of [static analysis](https://github.com/aviatesk/JET.jl) and [automatic differentiation](https://github.com/JuliaDiff/Diffractor.jl).

## Space
The [James Webb Space Telescope](https://www.jwst.nasa.gov/) is fully deployed, which I think is understood to be a big deal.

NASA's [Psyche](https://psyche.asu.edu/) mission is planned to launch this year, although it won't reach its destination until 2026. I'm especially interested in the Deep Space Optical Communications demonstration instrument on board. Even with the [technology involved](https://indico.physics.lbl.gov/event/815/attachments/1750/2119/APH_110_2018.pdf) I'm still astonished that it's possible.

## Search
There's a feeling in the air that it's time for a new generation of search engines. I signed up for the [Kagi Search](https://kagi.com/) private beta and within a day set it as my browser default. [Searx](https://searx.github.io/searx/) had its 1.0 release last year. It seems to me that [search.marginalia.nu](https://search.marginalia.nu/) has been received very warmly, and [Wiby](https://wiby.me/) has gotten more attention. I look forward to learning whether there's a future for niche, curated, or anti-commericial search; whether we'll see a revival of early-web-search serendipity; and whether people will pay for a high-quality search engine.

## Books
Historian of science Cyrus Mody, author of *Instrumental Community* and *The Long Arm of Moore's Law*, has another book coming out this year: [*The Squares: US Physical and Engineering Scientists in the Long 1970s*](https://mitpress.mit.edu/books/squares). It's still somewhat astounding for me what a force US military/defense research spending was in the postwar period,{% note() %} For example, see Paul Forman, [Behind Quantum Electronics: National Security as a Basis for Physical Research in the United States, 1940-1960](https://sci-hub.st/https://www.jstor.org/stable/27757599), *Historical Studies in the Physical and Biological Sciences* **18**, no. 1 (1987): 149-299. https://doi.org/10.2307/27757599 {% end %} and I don't have a good sense of how or to what extent a transition away from that happened. It sounds like that's just one piece of the story of this book ("the 'civilianization' of the US semiconductor industry" sounds particularly interesting), and I look forward to reading the whole.