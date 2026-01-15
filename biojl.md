+++
using Dates

date = Date("2020-01-23")
author = "sabrina"
+++

# Bio.jl is old and deprecated

![biojulia logo](/assets/biojulia-logo1.png)

Hi there! There have been incidents of confusion where newer users have tried to install and run an old and deprecated BioJulia package called `Bio.jl`, or they have not known which package(s) they need to install in order to start working.

So I'd like to take the opportunity to clear this situation up and perhaps put out a clearer explanation, of why Bio.jl exists when there are other packages with overlapping functionality.

Bio.jl was the first package BioJulia produced, at a time when the scale of the project meant it made sense to have a single module - Bio - with several submodules

    `Seq`, `Align`, `Phylo`, `Intervals`, `Structure`, `Var`, `Services`, `Tools`.

Bio has existed since very early days - or versions - of julia as well.

Eventually there came a point where datatype and algorithm specific packages made more sense than a single monolithic repository.

And so the package got split into many:

- `Bio.Seq` became [`BioSequences.jl`](https://github.com/BioJulia/BioSequences.jl/)
- `Bio.Align` became [`BioAlignments.jl`](https://github.com/BioJulia/BioAlignments.jl/)
- `Bio.Intervals` became [`GenomicFeatures.jl`](https://github.com/BioJulia/GenomicFeatures.jl/)
- `Bio.Structure` became [`BioStructures.jl`](https://github.com/BioJulia/BioStructures.jl/)
- `Bio.Var` became [`GeneticVariation.jl`](https://github.com/BioJulia/GeneticVariation.jl/)
- `Bio.Phylo` became [`Phylogenies.jl`](https://github.com/BioJulia/Phylogenies.jl/)
- `Bio.Services` became [`BioServices.jl`](https://github.com/BioJulia/BioServices.jl/)
- `Bio.Tools` became [`BioTools.jl`](https://github.com/BioJulia/BioTools.jl/)

`Bio.jl` then basically persisted as a convenience wrapper around those packages, so that they could be installed with a single command and were distributed set to compatible versions.

With julia v0.7/v1.0 and the new `Pkg` and Project system the need for `Bio.jl` to provide that functionality became largely moot.

## So what should you do?

As of today, `Bio.jl` is available for installation, but mostly just to prevent old scripts and projects breaking.

It is not longer recommended that you use `Bio.jl`. Instead you should start a julia project and add just the BioJulia packages you want to use. For a brief description on how to do this, check out the getting started page.

Happy hacking.

Sabrina.
