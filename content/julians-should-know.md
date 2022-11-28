+++
title = "What should Julia users know?"
date = 2022-11-28
description = "You'll be more likely to look something up when you can tell it should exist"
+++

[Julia](https://julialang.org) is a programming language designed to get high performance with code that's easy to read and write. It's really good! You should try it. If you already have, here's my list of broadly useful things to be aware of that you might miss just by diving in.

I don't mean for this to be overwhelming. A good way to get into Julia is to start using it for a problem you're interested in, picking up as much as you need to get things done. But at some point you'll want to know what you don't know.

I've tried to organize things starting with the most important and basic information, both along the whole page and within each section. These are personal suggestions.{% aside() %} I'm an intermediate Julia user, having made some small contributions to the the ecosystem and having done a few years of development for private scientific projects. {% end %} If you have ideas about what should go here, let me know [on Twitter](https://twitter.com/MuireallPrase).

### Community

The [Discourse board](discourse.julialang.org/) is the best place for questions and general discussion.{% aside() %} In particular, it's more active than StackExchange. {% end %} There's also a [Slack](https://julialang.org/slack/), the [Forem](https://forem.julialang.org/) (a sort of community blog), and a [whole bunch of people](https://twitter.com/search?q=%23julialang&src=typed_query&f=user) worth following on Twitter.

[Contributing to the Julia ecosystem](https://julialang.org/contribute/) is a great way to get a handle on the tacit or idiomatic stuff you don't get out of documentation or blog posts.

A good way to find packages in a given domain is to browse [the GitHub Organizations that the community groups related packages into](https://julialang.org/community/organizations/). There are thousands of [registered packages](https://github.com/JuliaRegistries/General) in the ecosystem, and if you search or ask around on Discourse and Slack you might find what you're looking for—or at least inspiration.

### The language

I recommend reading through [the manual](https://docs.julialang.org/en/v1/manual/getting-started/) to at least [Documentation](https://docs.julialang.org/en/v1/manual/documentation/) as a start. From the later sections I'll single out the [Performance Tips](https://docs.julialang.org/en/v1/manual/performance-tips/) and [Style Guide](https://docs.julialang.org/en/v1/manual/style-guide/). It's not necessarily obvious, but those last two are very useful for understanding the language.{% aside() %} As far as style, the [Blue](https://github.com/invenia/BlueStyle) guidelines have more detailed recommendations. {% end %}

In the Julia REPL, you can type `?` to enter [help mode](https://docs.julialang.org/en/v1/stdlib/REPL/#Help-mode), where Julia will attempt to show documentation for anything you enter. Function documentation will often mention related functions, which is useful for discovery. The standard library has [InteractiveUtils.methodswith](https://docs.julialang.org/en/v1/stdlib/InteractiveUtils/#InteractiveUtils.methodswith), which can help you discover methods if you miss finding class methods in an object oriented language with tab completion.

I find it pays off to skim documentation even for basics like [numbers](https://docs.julialang.org/en/v1/base/numbers/), [strings](https://docs.julialang.org/en/v1/base/strings/), and [arrays](https://docs.julialang.org/en/v1/base/arrays/), at least to get an idea of the kind of affordances Julia provides. You'll be more likely to look something up when you can tell it should exist.

For example, I'll call out the [collections and data structures](https://docs.julialang.org/en/v1/base/collections/) and [iteration utilities](https://docs.julialang.org/en/v1/base/iterators/), some of which I wouldn't have guessed were built into the language but which are very useful.

Similarly, there are [mathematical operators](https://docs.julialang.org/en/v1/base/math/) in base Julia it's worth knowing exist: `mod2pi` and `rem2pi` and the functions `sincos`, `cis`, `sinpi`, `sind`, and so on for trigonometry saving some effort and numerical exactness; similarly, `expm1` and  `log1p`; `hypot` and `LinearAlgebra.norm` for vector norm calculations avoiding overflow and underflow; various other utilities like `clamp` and  `mod1`.

The manual's [noteworthy differences from other languages](https://docs.julialang.org/en/v1/manual/noteworthy-differences/) mentions a wide assortment of features and conventions even if you're not coming from MATLAB, R, Python, C/C++, or Common Lisp.

Stefan Karpinski's 2019 talk [The Unreasonable Effectiveness of Multiple Dispatch](https://www.youtube.com/watch?v=kc9HwsxE1OY) is great if you want to understand why some people like Julia so much, along with some of the choices Julia makes as a language.{% note() %} I don't know if it belongs in the canon, but my favorite JuliaCon talk may be [Taking Vector Transposes Seriously](https://www.youtube.com/watch?v=C2RO34b_oPM) from Jiahao Chen in 2017. It's about Julia pre-1.0, so be careful—for example, these days the single quote gives you the adjoint, not the transpose. {% end %}

### Workflow

For workflow basics, start with [the Julia REPL](https://docs.julialang.org/en/v1/stdlib/REPL/#The-Julia-REPL), [Workflow Tips](https://docs.julialang.org/en/v1/manual/workflow-tips/), and the package manager [documentation](https://pkgdocs.julialang.org/dev/) up through [working with environments](https://pkgdocs.julialang.org/dev/environments/). If you're developing a package, [Revise.jl](https://timholy.github.io/Revise.jl/stable/) is basically mandatory to avoid constantly restarting Julia.{% aside() %} Even if you're just loading code from a file using `include`, Revise gives you the `includet` method for "include and track", so if you edit the file the changes are automatically loaded in your Julia session. I think some people miss this feature because it's not the headline use case for Revise, but it's nice. {% end %}

VS Code with [the Julia extension](https://www.julia-vscode.org/docs/dev/) is the recommended editor. Some of what you'll find in [the user guide for Julia in VS Code](https://www.julia-vscode.org/docs/dev/) you'd expect from any IDE—formatting, linting, running code—and some of it is Julia-specific, like using [sysimages](https://www.julia-vscode.org/docs/dev/userguide/compilesysimage/) to start sessions faster (via [PackageCompiler](https://julialang.github.io/PackageCompiler.jl/stable/sysimages.html)).

- [Pluto](https://github.com/fonsp/Pluto.jl) gives you a notebook like Jupyter, but without hidden state from out-of-order execution and with a source file that's valid Julia
- [UnicodePlots](https://github.com/JuliaPlots/UnicodePlots.jl) is a surprisingly richly featured backend for Julia's main plotting interface [Plots.jl](https://github.com/JuliaPlots/Plots.jl) that works in a terminal
- [PrettyTables](https://github.com/ronisbr/PrettyTables.jl) prints tabular data in a terminal in a very readable way
- [OhMyREPL](https://kristofferc.github.io/OhMyREPL.jl/latest/) adds some features to the Julia REPL like customizable syntax highlighting and rainbow parethesis matching
- [PackageCompiler](https://julialang.github.io/PackageCompiler.jl/stable/), mentioned above, can be used with or without the VS Code extension
- [PkgTemplates](https://github.com/JuliaCI/PkgTemplates.jl) is the canonical tool for creating new packages—which isn't hard to do by hand, but PkgTemplates is friendlier and can be customized to set up a repository configured for CI, code coverage, documentation, and so on
- [JuliaFormatter](https://github.com/domluna/JuliaFormatter.jl) is a customizable code formatter that also integrates well with the VS Code extension

### The Parameters pattern
I work with modeling problems involving many instances of components each with many parameters. It's hard to manage this situation elegantly together with requirements like default parameters, keyword constructors, efficient access to and mutation of parameters, lightweight representations that can be used directly in optimizers and differential equations, and so on. It's enough of a frustration in other languages that it gets its own heading here.

- One option is to use `NamedTuple`s to hold parameters. You might like [NamedTupleTools](https://github.com/JeffreySarnoff/NamedTupleTools.jl) which makes some things more straightforward. Also, don't miss that [property destructuring](https://docs.julialang.org/en/v1/manual/functions/#Property-destructuring) syntax was added in 1.8.
- The next step up is probably to define `struct`s using [`Base.@kwdef` ](https://github.com/JuliaLang/julia/blob/5495b8d67a66720559cfd8c13ebb315a80e4e579/base/util.jl#L492) to automatically get keyword constructors with default fields ([Parameters.jl](https://github.com/mauro3/Parameters.jl) also does this, but it's not necessary now that `@kwdef` is all grown up{% aside() %} it's been around for a while, but for obscure reasons `@kwdef` will only be exported and part of the public API as of Julia 1.9 {% end %} )
- [Accessors](https://github.com/JuliaObjects/Accessors.jl) (successor to [Setfield](https://github.com/jw3126/Setfield.jl)) gives you a simple way to update immutable data structures
- [StructArrays](https://juliaarrays.github.io/StructArrays.jl/stable/) defines an array type that acts like an array of `struct` elements but is stored internally as a list of arrays (potentially allowing, for example, effective use of SIMD without sacrificing ergonomics; see [AoS and SoA](https://en.wikipedia.org/wiki/AoS_and_SoA))
- [ComponentArrays](https://github.com/jonniedie/ComponentArrays.jl) is a really nice implementation of array types that act like a mutable `NamedTuple` or `struct`, but which compose with DifferentialEquations.jl, Optim.jl, or really anything that expects arrays
- If you find yourself reaching for this design pattern, [ModelingToolkit.jl](https://mtk.sciml.ai/stable/) might interest you

### Other packages

Some of the above are taken from the October 2022 thread ["Packages all Julians should know about"](https://discourse.julialang.org/t/packages-all-julians-should-know-about/88099) on the Julia Discourse board. Here are some more:

- [Documenter](https://documenter.juliadocs.org/stable/) is what people use to make documentation, and it has some good features like doctests and cross references worth getting familiar with
- [Literate.jl](https://fredrikekre.github.io/Literate.jl/v2/) is a package for [Literate Programming](https://en.wikipedia.org/wiki/Literate_programming) that lets you generate markdown for Documenter or a Jupyter notebook from the same source file
- [Plots.jl](https://github.com/JuliaPlots/Plots.jl) with your backend of choice is fine, but I'd recommend looking at [Makie](https://docs.makie.org/stable/), especially for interactivity{% note() %} although Plots.jl does have [the PlotlyJS backend](http://juliaplots.org/PlotlyJS.jl/stable/) {% end %} and performance (with an OpenGL backend)—[Beautiful Makie](https://beautiful.makie.org/dev/) has good examples
- [DataStructures.jl](https://github.com/JuliaCollections/DataStructures.jl) implements standard data structures
- [DataFrames.jl](https://github.com/JuliaData/DataFrames.jl) implements pandas-like DataFrames—don't miss the [tutorial by Bogumił Kamiński](https://github.com/bkamins/Julia-DataFrames-Tutorial) 
- [Memoize.jl](https://github.com/JuliaCollections/Memoize.jl) gives you easy memoization (there's also [Memoization.jl](https://github.com/marius311/Memoization.jl), which at this point may be more general than Memoize)
- [MacroTools.jl](https://github.com/FluxML/MacroTools.jl) is handy if you're writing macros
- [Transducers.jl](https://juliafolds.github.io/Transducers.jl/dev) gives you transducers, which you might know [from Clojure](https://clojure.org/reference/transducers){% note() %} [this description of good use cases for transducers](https://clojure.org/guides/faq#transducers_vs_seqs) is good to have in the back of your head {% end %}
- The packages under the [JuliaMath](https://github.com/JuliaMath) GitHub Organization include special functions, intervals, interpolations, root finding, and numerical integration, among others
- [JuliaDiff](https://juliadiff.org/) has various automatic differentiation packages under its umbrella

Of course there are also more domain-specific organizations and libraries that might as well be standard, like [JuliaGraphs](https://github.com/JuliaGraphs/)/[Graphs.jl](https://github.com/JuliaGraphs/Graphs.jl) for graph things or [JuliaDSP](https://github.com/JuliaDSP)/[DSP.jl](https://docs.juliadsp.org/stable/contents/){% aside() %} that's where the phase unwrapping utility is, by the way {% end %} for digital signal processing; canonical libraries that have their particular ways of doing things but are nonetheless very generic, like [Flux](https://fluxml.ai/Flux.jl/stable/) for machine learning; even things outside Julia's advertised wheelhouse like [Franklin](https://github.com/tlienart/Franklin.jl) for static site generation and the web framework [Genie](https://github.com/GenieFramework/Genie.jl).

### Performance, correctness, analysis
Start with [Unit Testing](https://docs.julialang.org/en/v1/stdlib/Test/) and the [Performance Tips](https://docs.julialang.org/en/v1/manual/performance-tips/) in the Julia manual, as well as the section on [Profiling](https://docs.julialang.org/en/v1/manual/profile/). There's also [Logging](https://docs.julialang.org/en/v1/stdlib/Logging/) in the standard library.

- TestItems/[TestItemRunner](https://github.com/julia-vscode/TestItemRunner.jl) are works in progress but very promising for improving testing workflows
- [BenchmarkTools]( https://juliaci.github.io/BenchmarkTools.jl/stable/) gives you better ways to benchmark than using `@time` to time commands
- [ProfileView](https://github.com/timholy/ProfileView.jl) is a visualizer for the results of profiling (one of several; the VS Code extension also has its own)
- [Infiltrator](https://github.com/JuliaDebug/Infiltrator.jl) gives you a macro that acts as a breakpoint
- [StaticArrays](https://github.com/JuliaArrays/StaticArrays.jl); [torrance](https://discourse.julialang.org/t/packages-all-julians-should-know-about/88099/16) on the Discourse thread explains it well:
    > This package allows for small, statically sized arrays. Because their size is known at compile time all sorts of optimisations and efficiencies kick in. Linear algebra operations, for example, are customised at compile time for the specific size of your matrix or array. For me, however, the biggest win is that static arrays are isbits, meaning these will be allocated on the stack not the heap, so these are ideal for cases where you’re working with small arrays of a known size in hot loops.
- [Tullio](https://github.com/mcabbott/Tullio.jl) is a neat way to write tensor operations that will take advantage of multithreading, SIMD (with [LoopVectorization](https://github.com/JuliaSIMD/LoopVectorization.jl)), and other tricks to go fast
- [JET](https://aviatesk.github.io/JET.jl/stable/) and [Cthulhu](https://github.com/JuliaDebug/Cthulhu.jl) do type-level program analysis that can catch bugs and type-unstable code
- People seem to be adopting [Aqua](https://github.com/JuliaTesting/Aqua.jl) for some other checks

### Cool stuff

[JuMP](https://jump.dev/) and its supporting packages for mathematical optimization as well as [DifferentialEquations.jl](https://diffeq.sciml.ai/stable/) are probably the best in their respective classes in any language.

- [Cassette](https://github.com/JuliaLabs/Cassette.jl) lets you do custom compiler passes, which enables all sorts of cool things
- I mentioned I was excited about [Symbolics.jl](https://symbolics.juliasymbolics.org/stable/)/[SymbolicUtils](https://symbolicutils.juliasymbolics.org/) back [in January](https://muireall.space/exciting-2022/). They've made a lot of progress but still suffer from the limitations I mentioned then:
    > The home page calls it a Computer Algebra System, but right now developers seem more focused on symbolic-numeric computation. It's in an odd situation where it has trouble simplifying arithmetic expressions with nested subtraction and division, but it can dramatically accelerate differential equation solvers. I think the potential here is underappreciated in scientific computing.
- [Metatheory.jl](https://github.com/JuliaSymbolics/Metatheory.jl), the e-graph rewriting backend for Symbolics
- [Diffractor.jl](https://github.com/JuliaDiff/Diffractor.jl) for autodiff

Again, [I'm on Twitter](https://twitter.com/MuireallPrase) if you have more tips.