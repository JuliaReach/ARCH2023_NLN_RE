# ARCH2023 NLN

This is the JuliaReach repeatability evaluation (RE) package for the ARCH-COMP
2023 category report: Continuous and Hybrid Systems with Nonlinear Dynamics
of the 7th International Competition on Verifying Continuous and Hybrid Systems
(ARCH-COMP '23).

To cite the work, you can use:

```
@inproceedings{GerettiAABCFILMMSWZ23,
  author    = {Luca Geretti and
               Julien Alexandre Dit Sandretto and
               Matthias Althoff and
               Luis Benet and
               Pieter Collins and
               Marcelo Forets and
               Elena Ivanova and
               Yangge Li and
               Sayan Mitra and
               Stefan Mitsch and
               Christian Schilling and
               Mark Wetzlinger and
               Daniel Zhuang},
  editor    = {Goran Frehse and
               Matthias Althoff},
  title     = {{ARCH-COMP23} Category Report: Continuous and Hybrid Systems with
               Nonlinear Dynamics},
  booktitle = {{ARCH}},
  series    = {EPiC Series in Computing},
  volume    = {96},
  pages     = {61--88},
  publisher = {EasyChair},
  year      = {2023},
  url       = {https://doi.org/10.29007/93f2},
  doi       = {10.29007/93f2}
}
```

## Installation

*Note:* Running the full benchmark suite should take no more than four hours
with a reasonable internet connection.

There are two ways to install and run this RE: either using the Julia script or
using the Docker script.
In both cases, first clone this repository.


**Using the Julia script.**
First install the Julia compiler following the instructions
[here](http://julialang.org/downloads).
Once you have installed Julia, execute

```shell
$ julia startup.jl
```

to run all the benchmarks.


**Using the Docker container.**
To build the container, you need the program `docker`.
For installation instructions on different platforms, consult
[the Docker documentation](https://docs.docker.com/install/).
For general information about `Docker`, see
[this guide](https://docs.docker.com/get-started/).
Once you have installed Docker, start the `measure_all` script:

```shell
$ ./measure_all
```

---

The Docker container can also be run interactively:

```shell
$ docker run -it juliareach bash

$ julia

julia> include("startup.jl")
```

## Outputs

After the benchmark runs have finished, the results will be stored in the folder
`result` and plots are generated in your working directory.

---

## How the Julia environment was created

```julia
julia> ]

(@v1.8) pkg> activate .
  Activating new environment at `.../ARCH2023_NLN/Project.toml`

pkg> add BenchmarkTools
pkg> add CSV
pkg> add DataFrames
pkg> add LaTeXStrings
pkg> add Plots
pkg> add ReachabilityAnalysis
```
