---
layout: page
title: "Current Environment"
category: community
date: 2016-10-19 21:08:18
---

A knowledge base of data science and machine learning tools and algorithms written in Haskell that either already exist or we would like to exist.

Note: some libraries are mentioned more than once, because they provide functionality that covers a few areas, however for clarity the links and project descriptions are only given at their first occurrence.

## Visualization 

- **Chart** [](https://github.com/timbod7/haskell-chart){:.github} [![Hackage](https://img.shields.io/hackage/v/Chart.svg)](https://hackage.haskell.org/package/Chart) [![Chart](http://stackage.org/package/Chart/badge/nightly)](http://stackage.org/nightly/package/Chart) : A library for generating 2D Charts and Plots, with backends provided by Cairo (http://hackage.haskell.org/package/Chart-cairo) and Diagrams (http://hackage.haskell.org/package/Chart-diagrams). Documentation: https://github.com/timbod7/haskell-chart/wiki.
- **plotlyhs** [](https://github.com/diffusionkinetics/open/tree/master/plotlyhs){:.github} [![Hackage](https://img.shields.io/hackage/v/plotlyhs.svg)](https://hackage.haskell.org/package/plotlyhs)  [![plotlyhs](http://stackage.org/package/plotlyhs/badge/nightly)](http://stackage.org/nightly/package/plotlyhs) :  This is a library for generating JSON value to use with the Plotly.js library. The interface directly reflects the structure of the Plotly.js library and is therefore quite low-level. Lenses are used throughout to set Maybe fields in records to provide both data and configuration options.
This library does not attempt to communicate with the Plotly API in any other way. All generated plots can be hosted on stand-alone web pages.
- **plots**  [](https://github.com/cchalmers/plots){:.github}  [![Hackage](https://img.shields.io/hackage/v/plots.svg)](https://hackage.haskell.org/package/plots)  [![plots](http://stackage.org/package/plots/badge/nightly)](http://stackage.org/nightly/package/plots): `Diagrams`-based plotting library.
- **hvega** [![Hackage](https://img.shields.io/hackage/v/hvega.svg)](https://hackage.haskell.org/package/hvega)  [![hvega](http://stackage.org/package/hvega/badge/nightly)](http://stackage.org/nightly/package/hvega): Support the creation of [Vega-Lite](https://vega.github.io/vega-lite/) visualizations in Haskell. 

## Publication

- **knit** [](https://github.com/adamConnerSax/knit-haskell){:.github} [![Hackage](https://img.shields.io/hackage/v/knit-haskell.svg)](https://hackage.haskell.org/package/knit-haskell)  [![knit](http://stackage.org/package/knit-haskell/badge/nightly)](http://stackage.org/nightly/package/knit-haskell): knit-haskell is a beginning attempt at bringing some of the benefits of Rmarkdown to Haskell. It includes an effects stack (using polysemy rather than mtl) which includes logging, randomness (via random-fu), a simplified interface to Pandoc and various writer-like effects to intersperse document building with regular code. Various helper functions are provided to simplify common operations, making it especially straightforward to build an HTML document from bits of markdown, latex and Lucid or Blaze html. Support is also included for including hvega visualizations.
- **pandoc-pyplot** [![Hackage](https://img.shields.io/hackage/v/pandoc-pyplot.svg)](https://hackage.haskell.org/package/pandoc-pyplot)  [![pandoc-pyplot](http://stackage.org/package/pandoc-pyplot/badge/nightly)](http://stackage.org/nightly/package/pandoc-pyplot): A Pandoc filter to include figures generated from Python code blocks. Keep the document and Python code in the same location. Output from Matplotlib is captured and included as a figure.


## Data structures

### Data frames

- **Frames** [![Hackage](https://img.shields.io/hackage/v/Frames.svg)](https://hackage.haskell.org/package/Frames) [![Frames](http://stackage.org/package/Frames/badge/nightly)](http://stackage.org/nightly/package/Frames) : User-friendly, type safe, runtime efficient tooling for working with tabular data deserialized from comma-separated values (CSV) files. The type of each row of data is inferred from data, which can then be streamed from disk, or worked with in memory. Also see the comprehensive [tutorial](https://acowley.github.io/Frames/)
- **Frames-map-reduce** [](https://github.com/adamConnerSax/frames-map-reduce){:.github} [![Hackage](https://img.shields.io/hackage/v/Frames-map-reduce.svg)](https://hackage.haskell.org/package/Frames-map-reduce) [![Frames-map-reduce](http://stackage.org/package/Frames-map-reduce/badge/nightly)](http://stackage.org/nightly/package/Frames-map-reduce) : This library contains some useful functions for using the map-reduce-folds package with Frames (containers of data rows) from the Frames package. Included, in Frames.MapReduce, are helpers for filtering Frames, splitting records into key and data columns and reattaching key columns after reducing.
Also included, in the Frames.Folds module, are some helpful functions for building folds of Frames from folds over each column, specified either individually or via a constraint on all the columns being folded over.
- **analyze** [](https://github.com/DataHaskell/dh-core){:.github} [![Hackage](https://img.shields.io/hackage/v/analyze.svg)](https://hackage.haskell.org/package/analyze)  [![analyze](http://stackage.org/package/analyze/badge/nightly)](http://stackage.org/nightly/package/analyze) : `pandas`-like dataframe operations for tabular data with CSV interface.
Currently maintained within the scope of the [DataHaskell `dh-core` project](https://github.com/datahaskell/dh-core).
- **bookkeeper** [![Hackage](https://img.shields.io/hackage/v/bookkeeper.svg)](https://hackage.haskell.org/package/bookkeeper)  [![bookkeeper](http://stackage.org/package/bookkeeper/badge/nightly)](http://stackage.org/nightly/package/bookkeeper) : A new take on datatypes and records using `OverloadedLabels` (which is available since GHC 8). It bears some similarities to Nikita Volkov's `record` library, but requires no Template Haskell.
- **colonnade** [](https://github.com/andrewthad/colonnade){:.github} [![Hackage](https://img.shields.io/hackage/v/colonnade.svg)](https://hackage.haskell.org/package/colonnade)  [![colonnade](http://stackage.org/package/colonnade/badge/nightly)](http://stackage.org/nightly/package/colonnade) : The colonnade package provides a way to talk about columnar encodings and decodings of data. This package provides very general types and does not provide a way for the end-user to actually apply the columnar encodings they build to data. Most users will also want to one a companion packages that provides (1) a content type and (2) functions for feeding data into a columnar encoding:
    * lucid-colonnade for lucid html tables
    * blaze-colonnade for blaze html tables
    * reflex-dom-colonnade for reactive reflex-dom tables
    * yesod-colonnade for yesod widgets
    * siphon for encoding and decoding CSVs

### Streaming / Folds
 
- **map-reduce-folds** [](https://github.com/adamConnerSax/map-reduce-folds){:.github}  [![Hackage](https://img.shields.io/hackage/v/map-reduce-folds.svg)](https://hackage.haskell.org/package/map-reduce-folds)  [![map-reduce-folds](http://stackage.org/package/map-reduce-folds/badge/nightly)](http://stackage.org/nightly/package/map-reduce-folds) : map-reduce-folds is an attempt to find a good balance between simplicity, performance, and flexibility for simple map/reduce style operations on a foldable container f of some type x (e.g., [x]). The goal of the package is to provide an efficient fold for the computation via the types in the foldl package.
Folds can be composed Applicatively, which makes it simple to do many such operations on the same data and loop over it only once.



### Arrays

- **vector** [![Hackage](https://img.shields.io/hackage/v/vector.svg)](https://hackage.haskell.org/package/vector)  [![vector](http://stackage.org/package/vector/badge/nightly)](http://stackage.org/nightly/package/vector) : An efficient implementation of Int-indexed arrays (both mutable and immutable), with a powerful loop optimisation framework.
- **contiguous** [](https://github.com/andrewthad/contiguous){:.github} [![Hackage](https://img.shields.io/hackage/v/contiguous.svg)](https://hackage.haskell.org/package/contiguous)  [![contiguous](http://stackage.org/package/contiguous/badge/nightly)](http://stackage.org/nightly/package/contiguous) : This package provides a typeclass Contiguous that offers a unified interface to working with Array, SmallArray, PrimArray, and UnliftedArray.
#### Multidimensional arrays
- **accelerate** [![Hackage](https://img.shields.io/hackage/v/accelerate.svg)](https://hackage.haskell.org/package/accelerate) [![accelerate](http://stackage.org/package/accelerate/badge/nightly)](http://stackage.org/nightly/package/accelerate) : Data.Array.Accelerate defines an embedded array language for computations for high-performance computing in Haskell. Computations on multi-dimensional, regular arrays are expressed in the form of parameterised collective operations, such as maps, reductions, and permutations. These computations may then be online compiled and executed on a range of architectures.
- **repa** [![Hackage](https://img.shields.io/hackage/v/repa.svg)](https://hackage.haskell.org/package/repa)  [![repa](http://stackage.org/package/repa/badge/nightly)](http://stackage.org/nightly/package/repa) : Repa provides high performance, regular, multi-dimensional, shape polymorphic parallel arrays. All numeric data is stored unboxed. 
- **massiv** [![Hackage](https://img.shields.io/hackage/v/massiv.svg)](https://hackage.haskell.org/package/massiv)  [![massiv](http://stackage.org/package/massiv/badge/nightly)](http://stackage.org/nightly/package/massiv) : Repa-style high-performance multi-dimentional arrays with nested parallelism and stencil computation capabilities.

### Records

- **vinyl** [![Hackage](https://img.shields.io/hackage/v/vinyl.svg)](https://hackage.haskell.org/package/vinyl)  [![labels](http://stackage.org/package/vinyl/badge/nightly)](http://stackage.org/nightly/package/vinyl) : Extensible records for Haskell with lenses. It has minimal dependencies and `Frames` is based on it.
- **labels** [![Hackage](https://img.shields.io/hackage/v/labels.svg)](https://hackage.haskell.org/package/labels)  [![labels](http://stackage.org/package/labels/badge/nightly)](http://stackage.org/nightly/package/labels) : Declare and access tuple fields with labels. An approach to anonymous records.
- **superrecord** [![Hackage](https://img.shields.io/hackage/v/superrecord.svg)](https://hackage.haskell.org/package/superrecord)  [![superrecord](http://stackage.org/package/superrecord/badge/nightly)](http://stackage.org/nightly/package/superrecord) [](https://github.com/agrafix/superrecord){:.github} Supercharged anonymous records. Introductory [blogpost](https://www.athiemann.net/2017/07/02/superrecord.html), with case study using ReaderT.


### Graphs

  - **algebraic-graphs** [![Hackage](https://img.shields.io/hackage/v/algebraic-graphs.svg)](https://hackage.haskell.org/package/algebraic-graphs) [![algebraic-graphs](http://stackage.org/package/algebraic-graphs/badge/nightly)](http://stackage.org/nightly/package/algebraic-graphs) : `algebraic-graphs` (a.k.a. `alga`) is a library for algebraic construction and manipulation of graphs in Haskell. See [this paper](https://github.com/snowleopard/alga-paper) for the motivation behind the library, the underlying theory and implementation details.
The top-level module `Algebra.Graph` defines the core data type `Graph`, which is a deep embedding of four graph construction primitives `empty`, `vertex`, `overlay` and `connect`. To represent non-empty graphs, see `Algebra.Graph.NonEmpty`. More conventional graph representations can be found in `Algebra.Graph.AdjacencyMap` and `Algebra.Graph.Relation`.
The type classes defined in `Algebra.Graph.Class` and `Algebra.Graph.HigherKinded.Class` can be used for polymorphic graph construction and manipulation. Also see `Algebra.Graph.Fold` that defines the Boehm-Berarducci encoding of algebraic graphs and provides additional flexibility for polymorphic graph manipulation.
  - **fgl** [![Hackage](https://img.shields.io/hackage/v/fgl.svg)](https://hackage.haskell.org/package/fgl) [![fgl](http://stackage.org/package/fgl/badge/nightly)](http://stackage.org/nightly/package/fgl) : An inductive representation of manipulating graph data structures. Original website can be found at http://web.engr.oregonstate.edu/~erwig/fgl/haskell.
  
### Trees

  - **tree-traversals** [![Hackage](https://img.shields.io/hackage/v/tree-traversals.svg)](https://hackage.haskell.org/package/tree-traversals)  [![tree-traversals](http://stackage.org/package/tree-traversals/badge/nightly)](http://stackage.org/nightly/package/tree-traversals) : The tree-traversals package defines in-order, pre-order, post-order, level-order, and reversed level-order traversals for tree-like types, and it also provides newtype wrappers for the various traversals so they may be used with `traverse`.
  - **KdTree**  [](https://github.com/binarysunrise-io/kdtree){:.github} [![Hackage](https://img.shields.io/hackage/v/KdTree.svg)](https://hackage.haskell.org/package/KdTree)  [![KdTree](http://stackage.org/package/KdTree/badge/nightly)](http://stackage.org/nightly/package/KdTree) : A simple library for k-d trees in Haskell. It enables searching through collections of points in O(log N) average time, using the nearestNeighbor function.


## Database interfaces

- **beam** [Homepage](http://tathougies.github.io/beam/) [![Hackage](https://img.shields.io/hackage/v/beam-core.svg)](https://hackage.haskell.org/package/beam-core) [![beam-core](http://stackage.org/package/beam-core/badge/nightly)](http://stackage.org/nightly/package/beam-core) : Beam is a highly-general library for accessing any kind of database with Haskell. It supports several backends. beam-postgres and beam-sqlite are included in the main beam repository. Others are hosted and maintained independently, such as beam-mysql and beam-firebird. The documentation here shows examples in all known backends.
Beam is highly extensible and other backends can be shipped independently without requiring any changes in the core libraries.For information on creating additional SQL backends, see the manual section for more.
- **selda** [](https://github.com/valderman/selda){:.github} [![Hackage](https://img.shields.io/hackage/v/selda.svg)](https://hackage.haskell.org/package/selda) [![selda](http://stackage.org/package/selda/badge/nightly)](http://stackage.org/nightly/package/selda) : Selda is a Haskell library for interacting with SQL-based relational databases inspired by LINQ and Opaleye.
- **relational-record** [Homepage](http://khibino.github.io/haskell-relational-record) [![Hackage](https://img.shields.io/hackage/v/relational-record.svg)](https://hackage.haskell.org/package/relational-record)  [![relational-record](http://stackage.org/package/relational-record/badge/nightly)](http://stackage.org/nightly/package/relational-record) : Haskell Relational Record (HRR) is a query generator based on typed relational algebra and correspondence between SQL value lists and Haskell record types, which provide programming interfaces to Relational DataBase Managemsnt Systems (RDBMS).




## Numerical linear algebra

- **hmatrix** [![Hackage](https://img.shields.io/hackage/v/hmatrix.svg)](https://hackage.haskell.org/package/hmatrix)  [![hmatrix](http://stackage.org/package/hmatrix/badge/nightly)](http://stackage.org/nightly/package/hmatrix) : Bindings to BLAS/LAPACK. Linear solvers, matrix decompositions, and more.
- **dense-linear-algebra** [](http://github.com/DataHaskell/dh-core/){:.github}  [![Hackage](https://img.shields.io/hackage/v/dense-linear-algebra.svg)](https://hackage.haskell.org/package/dense-linear-algebra)  [![dense-linear-algebra](http://stackage.org/package/dense-linear-algebra/badge/nightly)](http://stackage.org/nightly/package/dense-linear-algebra) : A collection of linear-algebra related modules, extracted from the `statistics` library. Matrices and vectors are internally represented with unboxed `vector`s, and the algorithms rely on in-place mutation for high efficiency. 
Currently maintained within the scope of the [DataHaskell `dh-core` project](https://github.com/datahaskell/dh-core).
- **sparse-linear-algebra** [![Hackage](https://img.shields.io/hackage/v/sparse-linear-algebra.svg)](https://hackage.haskell.org/package/sparse-linear-algebra) [![sparse-linear-algebra](http://stackage.org/package/sparse-linear-algebra/badge/nightly)](http://stackage.org/nightly/package/sparse-linear-algebra) : Native library for sparse algebraic computation. Linear solvers, matrix decompositions and related tools; functional but not optimized for efficiency yet.
- **linearEqSolver** [](http://github.com/LeventErkok/linearEqSolver){:.github} [![Hackage](https://img.shields.io/hackage/v/linearEqSolver.svg)](https://hackage.haskell.org/package/linearEqSolver) [![linearEqSolver](http://stackage.org/package/linearEqSolver/badge/nightly)](http://stackage.org/nightly/package/linearEqSolver) : Solve linear systems of equations over integers and rationals, using an SMT solver.

## Generation of random data

  - **mwc-probability**  [![Hackage](https://img.shields.io/hackage/v/mwc-probability.svg)](https://hackage.haskell.org/package/mwc-probability)  [![mwc-probability](http://stackage.org/package/mwc-probability/badge/nightly)](http://stackage.org/nightly/package/mwc-probability) : A simple probability distribution type, where distributions are characterized by sampling functions. Simple and idiomatic interface based on Applicative and Monad instances.
  - **random-fu**  [![Hackage](https://img.shields.io/hackage/v/random-fu.svg)](https://hackage.haskell.org/package/random-fu)  [![random-fu](http://stackage.org/package/random-fu/badge/nightly)](http://stackage.org/nightly/package/random-fu) : Random number generation based on modeling random variables in two complementary ways: first, by the parameters of standard mathematical distributions and, second, by an abstract type (RVar) which can be composed and manipulated monadically and sampled in either monadic or "pure" styles.
The primary purpose of this library is to support defining and sampling a wide variety of high quality random variables. Quality is prioritized over speed, but performance is an important goal too. Very flexible, providing both a concrete ('Distribution') and and abstract but composable ('RVar') view of random variables.
  
  
## Statistics

  - **statistics** [![Hackage](https://img.shields.io/hackage/v/statistics.svg)](https://hackage.haskell.org/package/statistics) [![statistics](http://stackage.org/package/statistics/badge/nightly)](http://stackage.org/nightly/package/statistics) : This library provides a number of common functions and types useful in statistics. We focus on high performance, numerical robustness, and use of good algorithms. Where possible, we provide references to the statistical literature.
The library's facilities can be divided into four broad categories:
    - Working with widely used discrete and continuous probability distributions. (There are dozens of exotic distributions in use; we focus on the most common.)
    - Computing with sample data: quantile estimation, kernel density estimation, histograms, bootstrap methods, significance testing, and regression and autocorrelation analysis.
    - Random variate generation under several different distributions.
    - Common statistical tests for significant differences between samples.
  - **foldl-statistics** [](https://github.com/data61/foldl-statistics){:.github} [![Hackage](https://img.shields.io/hackage/v/foldl-statistics.svg)](https://hackage.haskell.org/package/foldl-statistics) [![foldl-statistics](http://stackage.org/package/foldl-statistics/badge/nightly)](http://stackage.org/nightly/package/foldl-statistics) : A reimplementation of the Statistics.Sample module using the foldl package. The intention of this package is to allow these algorithms to be used on a much broader set of data input types, including lists and streaming libraries such as conduit and pipes, and any other type which is Foldable.
All statistics in this package can be computed with no more than two passes over the data - once to compute the mean and once to compute any statistics which require the mean.
  - **tdigest** [![Hackage](https://img.shields.io/hackage/v/tdigest.svg)](https://hackage.haskell.org/package/tdigest) [![tdigest](http://stackage.org/package/tdigest/badge/nightly)](http://stackage.org/nightly/package/tdigest) : A new data structure for accurate on-line accumulation of rank-based statistics such as quantiles and trimmed means.
  - **histogram-fill** [![Hackage](https://img.shields.io/hackage/v/histogram-fill.svg)](https://hackage.haskell.org/package/histogram-fill) [![histogram-fill](http://stackage.org/package/histogram-fill/badge/nightly)](http://stackage.org/nightly/package/histogram-fill) : A convenient way to create and fill histograms. It supports fixed- and variable-size bins, missing data and 2D binning.
  - **uncertain** [![Hackage](https://img.shields.io/hackage/v/uncertain.svg)](https://hackage.haskell.org/package/uncertain)  [![uncertain](http://stackage.org/package/uncertain/badge/nightly)](http://stackage.org/nightly/package/uncertain) : Provides tools to manipulate numbers with inherent experimental/measurement uncertainty, and propagates them through functions.
  - **measurable** [](https://github.com/jtobin/measurable){:.github} [![Hackage](https://img.shields.io/hackage/v/measurable.svg)](https://hackage.haskell.org/package/measurable)  [![measurable](http://stackage.org/package/measurable/badge/nightly)](http://stackage.org/nightly/package/measurable) :  Construct measures from samples, mass/density functions, or even sampling functions. Construct image measures by fmap-ing measurable functions over them, or create new measures from existing ones by measure convolution and friends provided by a simple Num instance enabled by an Applicative instance. Create measures from graphs of other measures using the Monad instance and do-notation.
Query measures by integrating meaurable functions against them. Extract moments, cumulative density functions, or probabilities.
Caveat: while fun to play with, and rewarding to see how measures fit together, measure operations as nested integrals are exponentially complex. Don't expect them to scale very far!
 


## Integration

- Markov Chain Monte Carlo
  - **declarative** [![Hackage](https://img.shields.io/hackage/v/declarative.svg)](https://hackage.haskell.org/package/declarative)  [![declarative](http://stackage.org/package/declarative/badge/nightly)](http://stackage.org/nightly/package/declarative) : A simple combinator language for Markov transition operators that are useful in MCMC.
  - **flat-mcmc** [![Hackage](https://img.shields.io/hackage/v/flat-mcmc.svg)](https://hackage.haskell.org/package/flat-mcmc) [![flat-mcmc](http://stackage.org/package/flat-mcmc/badge/nightly)](http://stackage.org/nightly/package/flat-mcmc) : flat-mcmc uses an ensemble sampler that is invariant to affine transformations of space. It wanders a target probability distribution's parameter space as if it had been "flattened" or "unstretched" in some sense, allowing many particles to explore it locally and in parallel.
In general this sampler is useful when you want decent performance without dealing with any tuning parameters or local proposal distributions.

- Dynamical systems
  - **numeric-ode** [](https://github.com/qnikst/numeric-ode){:.github} [![Hackage](https://img.shields.io/hackage/v/numeric-ode.svg)](https://hackage.haskell.org/package/numeric-ode)  [![numeric-ode](http://stackage.org/package/numeric-ode/badge/nightly)](http://stackage.org/nightly/package/numeric-ode) : Small project for different ODE solvers, in particular symplectic solvers.
This is very experimental and will change. The Störmer-Verlet generates a correct orbit for Jupiter but no guarantees are given for any of the other methods.

## Differentiation

- Automatic differentiation
  - **ad** [![Hackage](https://img.shields.io/hackage/v/ad.svg)](https://hackage.haskell.org/package/ad)  [![ad](http://stackage.org/package/ad/badge/nightly)](http://stackage.org/nightly/package/ad) : Automatic differentiation to arbitrary order, applicable to data provided in any Traversable container.
  - **backprop** [](https://github.com/mstksg/backprop){:.github} [![Hackage](https://img.shields.io/hackage/v/backprop.svg)](https://hackage.haskell.org/package/backprop) [![backprop](http://stackage.org/package/backprop/badge/nightly)](http://stackage.org/nightly/package/backprop) : Automatic heterogeneous back-propagation. Write your functions to compute your result, and the library will automatically generate functions to compute your gradient. Differs from `ad` by offering full heterogeneity -- each intermediate step and the resulting value can have different types. Mostly intended for usage with gradient descent and other numeric optimization techniques. Introductory blogpost [here](https://blog.jle.im/entry/introducing-the-backprop-library.html).


## Optimization

- Linear programming
  - **glpk-hs** [![Hackage](https://img.shields.io/hackage/v/glpk-hs.svg)](https://hackage.haskell.org/package/glpk-hs)  [![glpk-hs](http://stackage.org/package/glpk-hs/badge/nightly)](http://stackage.org/nightly/package/glpk-hs) : Friendly interface to GLPK's linear programming and mixed integer programming features. Intended for easy extensibility, with a general, pure-Haskell representation of linear programs. 
- Convex optimization
  - **optimization** [](https://github.com/bgamari/optimization){:.github} [![Hackage](https://img.shields.io/hackage/v/optimization.svg)](https://hackage.haskell.org/package/optimization) [![optimization](http://stackage.org/package/optimization/badge/nightly)](http://stackage.org/nightly/package/optimization) : A number of optimization techniques from the modern optimization literature (quasi-Newton, stochastic gradient descent, mirror descent, projected subgradient etc.).
  - **sgd** [](https://github.com/kawu/sgd){:.github} [![Hackage](https://img.shields.io/hackage/v/sgd.svg)](https://hackage.haskell.org/package/sgd)  [![sgd](http://stackage.org/package/sgd/badge/nightly)](http://stackage.org/nightly/package/sgd) : Stochastic gradient descent.


## Signal processing 

### Discrete/Fast Fourier Transform
- **contiguous-fft** [](https://github.com/bgamari/contiguous-fft){:.github} [![Hackage](https://img.shields.io/hackage/v/contiguous-fft.svg)](https://hackage.haskell.org/package/contiguous-fft) [![contiguous-fft](http://stackage.org/package/contiguous-fft/badge/nightly)](http://stackage.org/nightly/package/contiguous-fft) : DFT and iDFT on data structures implementing a common contiguous interface.

 

## Machine Learning frameworks
  - **probably-baysig** [](https://github.com/glutamate/probably-baysig){:.github} [![Hackage](https://img.shields.io/hackage/v/probably-baysig.svg)](https://hackage.haskell.org/package/probably-baysig) [![probably-baysig](http://stackage.org/package/probably-baysig/badge/nightly)](http://stackage.org/nightly/package/probably-baysig) : This library contains definitions and functions for probabilistic and statistical inference.
    - Math.Probably.Sampler defines the sampling function monad
    - Math.Probably.PDF defines some common parametric log-probability density functions
    - Math.Probably.FoldingStats defines statistics as folds that can be composed and calculated independently of the container of the underlying data.
    - Strategy.\* implements various transition operators for Markov Chain Monte Carlo, including Metropolis-Hastings, Hamiltonian Monte Carlo, NUTS, and continuous/discrete slice samplers.
    - Math.Probably.MCMC implements functions and combinators for running Markov chains and interleaving transition operators.
  - **mltool** [](https://github.com/aligusnet/mltool){:.github} [![Hackage](https://img.shields.io/hackage/v/mltool.svg)](https://hackage.haskell.org/package/mltool)  [![mltool](http://stackage.org/package/mltool/badge/nightly)](http://stackage.org/nightly/package/mltool) : Haskell Machine Learning Toolkit includes various methods of supervised learning: linear regression, logistic regression, SVN, neural networks, etc. as well as some methods of unsupervised methods: K-Means and PCA.


## Bayesian inference
### Nested sampling
  - **NestedSampling** [![Hackage](https://img.shields.io/hackage/v/NestedSampling.svg)](https://hackage.haskell.org/package/NestedSampling)  [![NestedSampling](http://stackage.org/package/NestedSampling/badge/nightly)](http://stackage.org/nightly/package/NestedSampling) : The code here is a fairly straightforward translation of the tutorial nested sampling code from Skilling and Sivia. The original code can be found at http://www.inference.phy.cam.ac.uk/bayesys/sivia/ along with documentation at http://www.inference.phy.cam.ac.uk/bayesys/. An example program called lighthouse.hs is included.
  - **NestedSampling-hs** [](https://github.com/eggplantbren/NestedSampling.hs){:.github} [![Hackage](https://img.shields.io/hackage/v/NestedSampling-hs.svg)](https://hackage.haskell.org/package/NestedSampling-hs)  [![NestedSampling-hs](http://stackage.org/package/NestedSampling-hs/badge/nightly)](http://stackage.org/nightly/package/NestedSampling-hs) : This is a Haskell implementation of the classic Nested Sampling algorithm introduced by John Skilling. You can use it for Bayesian inference, statistical mechanics, and optimisation applications, and it comes with a few example programs.


### Probabilistic programming languages
  - **monad-bayes** [](https://github.com/adscib/monad-bayes){:.github} [![Hackage](https://img.shields.io/hackage/v/monad-bayes.svg)](https://hackage.haskell.org/package/monad-bayes)  [![monad-bayes](http://stackage.org/package/monad-bayes/badge/nightly)](http://stackage.org/nightly/package/monad-bayes) : A library for probabilistic programming in Haskell using probability monads. The emphasis is on composition of inference algorithms implemented in terms of monad transformers. The code is still experimental, but will be released on Hackage as soon as it reaches relative stability. User's guide will appear soon. In the meantime see the models folder that contains several examples.
  - **hakaru** [](https://github.com/hakaru-dev/hakaru){:.github} [![Hackage](https://img.shields.io/hackage/v/hakaru.svg)](https://hackage.haskell.org/package/hakaru)  [![hakaru](http://stackage.org/package/hakaru/badge/nightly)](http://stackage.org/nightly/package/hakaru) : Hakaru is a simply-typed probabilistic programming language, designed for easy specification of probabilistic models and inference algorithms. Hakaru enables the design of modular probabilistic inference programs by providing:
      - A language for representing probabilistic distributions, queries, and inferences
      - Methods for transforming probabilistic information, such as conditional probability and probabilistic inference, using computer algebra
  - **deanie** [](https://github.com/jtobin/deanie){:.github} [![Hackage](https://img.shields.io/hackage/v/deanie.svg)](https://hackage.haskell.org/package/deanie)  [![deanie](http://stackage.org/package/deanie/badge/nightly)](http://stackage.org/nightly/package/deanie) : `deanie` is an embedded probabilistic programming language. It can be used to denote, sample from, and perform inference on probabilistic programs.



## Supervised learning

### Time-series filtering
  - Kalman filtering
    - **estimator** [![Hackage](https://img.shields.io/hackage/v/estimator.svg)](https://hackage.haskell.org/package/estimator)  [![estimator](http://stackage.org/package/estimator/badge/nightly)](http://stackage.org/nightly/package/estimator) : The goal of this library is to simplify implementation and use of state-space estimation algorithms, such as Kalman Filters. The interface for constructing models is isolated as much as possible from the specifics of a given algorithm, so swapping out a Kalman Filter for a Bayesian Particle Filter should involve a minimum of effort.
This implementation is designed to support symbolic types, such as from sbv or ivory. As a result you can generate code in another language, such as C, from a model written using this package; or run static analyses on your model.
    - **kalman** [![Hackage](https://img.shields.io/hackage/v/kalman.svg)](https://hackage.haskell.org/package/kalman)  [![kalman](http://stackage.org/package/kalman/badge/nightly)](http://stackage.org/nightly/package/kalman) : Linear, extended and unscented Kalman filters are provided, along with their corresponding smoothers. Furthermore, a particle filter and smoother is provided.


### Graphical models
  - Hidden Markov models
    - **HMM** [](https://github.com/mikeizbicki/hmm){:.github} [![Hackage](https://img.shields.io/hackage/v/HMM.svg)](https://hackage.haskell.org/package/HMM)  [![HMM](http://stackage.org/package/HMM/badge/nightly)](http://stackage.org/nightly/package/HMM) 
    - **hmm-hmatrix** [](http://hub.darcs.net/thielema/hmm-hmatrix){:.darcs} [![Hackage](https://img.shields.io/hackage/v/hmm-hmatrix.svg)](https://hackage.haskell.org/package/hmm-hmatrix)  [![hmm-hmatrix](http://stackage.org/package/hmm-hmatrix/badge/nightly)](http://stackage.org/nightly/package/hmm-hmatrix) : Hidden Markov Models implemented using HMatrix data types and operations. http://en.wikipedia.org/wiki/Hidden_Markov_Model 
It supports any kind of emission distribution, where discrete and multivariate Gaussian distributions are implemented as examples.
It currently implements:
      * generation of samples of emission sequences,
      * computation of the likelihood of an observed sequence of emissions,
      * construction of most likely state sequence that produces an observed sequence of emissions,
      * supervised and unsupervised training of the model by Baum-Welch algorithm.
    - **learning-hmm** [](https://github.com/mnacamura/learning-hmm){:.github} [![Hackage](https://img.shields.io/hackage/v/learning-hmm.svg)](https://hackage.haskell.org/package/learning-hmm)  [![learning-hmm](http://stackage.org/package/learning-hmm/badge/nightly)](http://stackage.org/nightly/package/learning-hmm) : This library provides functions for the maximum likelihood estimation of discrete hidden Markov models. At present, only Baum-Welch and Viterbi algorithms are implemented for the plain HMM and the input-output HMM.


### Classification
  - Linear discriminant analysis
    - **linda** [![Hackage](https://img.shields.io/hackage/v/linda.svg)](https://hackage.haskell.org/package/linda)  [![linda](http://stackage.org/package/linda/badge/nightly)](http://stackage.org/nightly/package/linda) : LINDA implements linear discriminant analysis. It provides both data classification (according to Fisher) and data analysis (by discriminant criteria). Due to the `hmatrix` dependency, this package needs LAPACK installed, too. 
  - Support Vector Machines
    - **svm-simple** [![Hackage](https://img.shields.io/hackage/v/svm-simple.svg)](https://hackage.haskell.org/package/svm-simple)  [![svm-simple](http://stackage.org/package/svm-simple/badge/nightly)](http://stackage.org/nightly/package/svm-simple) : A set of simplified bindings to [libsvm](http://www.csie.ntu.edu.tw/~cjlin/libsvm/) suite of support vector machines. This package provides tools for classification, one-class classification and support vector regression.
  - Decision trees
    - **hinduce-classifier-decisiontree** [](https://github.com/roberth/hinduce-classifier-decisiontree){:.github} [![Hackage](https://img.shields.io/hackage/v/hinduce-classifier-decisiontree.svg)](https://hackage.haskell.org/package/hinduce-classifier-decisiontree)  [![hinduce-classifier-decisiontree](http://stackage.org/package/hinduce-classifier-decisiontree/badge/nightly)](http://stackage.org/nightly/package/hinduce-classifier-decisiontree) : A very simple decision tree construction algorithm; an implementation of `hinduce-classifier`'s Classifier class.
    - **HaskellGBM** [](https://github.com/dpkatz/HaskellGBM){:.github} [![Hackage](https://img.shields.io/hackage/v/HaskellGBM.svg)](https://hackage.haskell.org/package/HaskellGBM) [![HaskellGBM](http://stackage.org/package/HaskellGBM/badge/nightly)](http://stackage.org/nightly/package/HaskellGBM) : Haskell wrapper around LightGBM, the distributed library for gradient-boosted decision tree algorithms. The emphasis is on using Haskell types (in particular the `refined` library) to help ensure that the hyperparameter settings chosen by the user are coherent and in-bounds at all times.
  - Gaussian processes
    - **HasGP** [![Hackage](https://img.shields.io/hackage/v/HasGP.svg)](https://hackage.haskell.org/package/HasGP)  [![HasGP](http://stackage.org/package/HasGP/badge/nightly)](http://stackage.org/nightly/package/HasGP) : Gaussian processes for regression and classification, based on the Laplace approximation and Expectation Propagation.

### Neural Networks
  - **neural** [](https://github.com/brunjlar/neural){:.github} [![Hackage](https://img.shields.io/hackage/v/neural.svg)](https://hackage.haskell.org/package/neural)  [![neural](http://stackage.org/package/neural/badge/nightly)](http://stackage.org/nightly/package/neural) : The goal of neural is to provide a modular and flexible neural network library written in native Haskell.
Features include
    - composability via arrow-like instances and pipes,
    - automatic differentiation for automatic gradient descent/ backpropagation training (using Edward Kmett's fabulous ad library).
The idea is to be able to easily define new components and wire them up in flexible, possibly complicated ways (convolutional deep networks etc.).
Four examples are included as proof of concept:
    - A simple neural network that approximates the sine function on [0,2 pi].
    - Another simple neural network that approximates the sqrt function on [0,4].
    - A slightly more complicated neural network that solves the famous Iris flower problem.
    - A first (still simple) neural network for recognizing handwritten digits from the equally famous MNIST database.
The library is still very much experimental at this point.
  - **backprop-learn** [](https://github.com/mstksg/backprop-learn){:.github} [![Hackage](https://img.shields.io/hackage/v/backprop-learn.svg)](https://hackage.haskell.org/package/backprop-learn)  [![grenade](http://stackage.org/package/backprop-learn/badge/nightly)](http://stackage.org/nightly/package/backprop-learn) : Combinators and types for easily building trainable neural networks using the 'backprop' library.
  - **grenade** [](https://github.com/HuwCampbell/grenade){:.github} [![Hackage](https://img.shields.io/hackage/v/grenade.svg)](https://hackage.haskell.org/package/grenade)  [![grenade](http://stackage.org/package/grenade/badge/nightly)](http://stackage.org/nightly/package/grenade) : Grenade is a composable, dependently typed, practical, and fast recurrent neural network library for precise specifications and complex deep neural networks in Haskell.
Grenade provides an API for composing layers of a neural network into a sequence parallel graph in a type safe manner; running networks with reverse automatic differentiation to calculate their gradients; and applying gradient decent for learning. Documentation and examples are available on github https://github.com/HuwCampbell/grenade.
  - **hasktorch** [](https://github.com/hasktorch/hasktorch){:.github} [![Hackage](https://img.shields.io/hackage/v/hasktorch.svg)](https://hackage.haskell.org/package/hasktorch)  [![hasktorch](http://stackage.org/package/hasktorch/badge/nightly)](http://stackage.org/nightly/package/hasktorch) : Hasktorch is a library for tensors and neural networks in Haskell. It is an independent open source community project which leverages the core C libraries shared by Torch and PyTorch. This library leverages cabal new-build and backpack.
Note that this project is in early development and should only be used by contributing developers. Expect substantial changes to the library API as it evolves.
  - **tensorflow** [![Hackage](https://img.shields.io/hackage/v/tensorflow.svg)](https://hackage.haskell.org/package/tensorflow) [![tensorflow](http://stackage.org/package/tensorflow/badge/nightly)](http://stackage.org/nightly/package/tensorflow) : Haskell bindings for Tensorflow.  
  - Recurrent Neural Networks
    - **grenade** 
  - Convolutional Neural Networks
    - **grenade** 
  - LSTM (Long Short-Term Memory)
    - **grenade** 
    - **neural** 
  - Convolutional Neural Networks
    - **tensorflow** 
  
  - Generative Neural Networks
 
  - References : [Neural Networks, Types, and Functional Programming](https://colah.github.io/posts/2015-09-NN-Types-FP/)

### Naive Bayes
  - Gaussian Naive Bayes
  - Multinomial Naive Bayes
  - Bernoulli Naive Bayes

### Boosting
  - XGBoost 
    - **xgboost-haskell** [![Hackage](https://img.shields.io/hackage/v/xgboost-haskell.svg)](https://hackage.haskell.org/package/xgboost-haskell)  [![xgboost-haskell](http://stackage.org/package/xgboost-haskell/badge/nightly)](http://stackage.org/nightly/package/xgboost-haskell) : XGBoost for Haskell, based on the foundation package. FFI binding of xgboost
    - **xgboost.hs** [](https://github.com/robertzk/xgboost.hs){:.github} 
  - AdaBoost    

### Regression

  - Nearest Neighbors
    - **HLearn** [](https://izbicki.me/blog/fast-nearest-neighbor-queries-in-haskell.html){:.blogpost} 
  
  - Linear Regression
    - **statistics**
    
  - Gaussian processes
    - **HasGP**
    
  - Kalman filtering
    - **kalman** 
    - **estimator** 
  

### Reinforcement learning
  - **reinforce** [](https://github.com/sentenai-research/reinforce){:.github} [![Hackage](https://img.shields.io/hackage/v/reinforce.svg)](https://hackage.haskell.org/package/reinforce)  [![reinforce](http://stackage.org/package/reinforce/badge/nightly)](http://stackage.org/nightly/package/reinforce) : `reinforce` exports an openai-gym-like typeclass, MonadEnv, with both an interface to [gym-http-api](https://github.com/openai/gym-http-api/), as well as haskell-native environments which provide a substantial speed-up to the http-server interface.
  - **gym-http-api** [](https://github.com/stites/gym-http-api){:github} [![Hackage](https://img.shields.io/hackage/v/gym-http-api.svg)](https://hackage.haskell.org/package/gym-http-api)  [![gym-http-api](http://stackage.org/package/gym-http-api/badge/nightly)](http://stackage.org/nightly/package/gym-http-api) : This library provides a REST client to the gym open-source library. gym-http-api itself provides a python-based REST server to the gym open-source library, allowing development in languages other than python. Note that the openai/gym-http-api is a monorepo of all language-clients. This hackage library tracks stites/gym-http-api which is the actively-maintained haskell fork.
  - Policy gradient

  - Q-Learning
    - Neural Network Q-Learning

## Clustering

  - K-Means
    - **kmeans** [](http://hub.darcs.net/gershomb/kmeans){:.darcs} [![Hackage](https://img.shields.io/hackage/v/kmeans.svg)](https://hackage.haskell.org/package/kmeans)  [![kmeans](http://stackage.org/package/kmeans/badge/nightly)](http://stackage.org/nightly/package/kmeans) : A simple implementation of the standard k-means clustering algorithm.
    - **clustering** [![Hackage](https://img.shields.io/hackage/v/clustering.svg)](https://hackage.haskell.org/package/clustering)  [![clustering](http://stackage.org/package/clustering/badge/nightly)](http://stackage.org/nightly/package/clustering) : Methods included in this library: Agglomerative hierarchical clustering: Complete linkage O(n^2), Single linkage O(n^2), Average linkage O(n^2), Weighted linkage O(n^2), Ward's linkage O(n^2). KMeans clustering.

  - Self-Organising Maps (SOM)
    - Hyperbolic-SOM
    - Hierarchical (H)SOMs

  - Mean-shift
  - Affinity propagation
  - Spectral Clustering
    - **spectral-clustering** [](https://github.com/GregorySchwartz/spectral-clustering){:github}  [![Hackage](https://img.shields.io/hackage/v/spectral-clustering.svg)](https://hackage.haskell.org/package/spectral-clustering)  [![spectral-clustering](http://stackage.org/package/spectral-clustering/badge/nightly)](http://stackage.org/nightly/package/spectral-clustering) : Spectral clustering of dense and sparse matrices.
  - Hierarchical clustering
    - **clustering** 
  - Birch

## Dimensionality reduction

  - Principal Component Analysis (PCA)
    - Kernel PCA
    - Incremental PCA
  - Truncated SVD*
  - Independent Component Analysis (ICA)
  - t-SNE (t-distributed stochastic neighbor embedding)
    - **tsne** [![Hackage](https://img.shields.io/hackage/v/tsne.svg)](https://hackage.haskell.org/package/tsne)  [![tsne](http://stackage.org/package/tsne/badge/nightly)](http://stackage.org/nightly/package/tsne) 
    
    
## Machine Learning Misc.
  - **sibe** [](https://github.com/mdibaiee/sibe){:.github} [![Hackage](https://img.shields.io/hackage/v/sibe.svg)](https://hackage.haskell.org/package/sibe) [![sibe](http://stackage.org/package/sibe/badge/nightly)](http://stackage.org/nightly/package/sibe) : A simple, experimental machine learning library. Contains implementations of 
    - Multi-class Naive Bayes classification 
    - Word2Vec word embedding 
    - Principal component analysis (PCA)
  - **aima-haskell** [](https://github.com/chris-taylor/aima-haskell){:.github} : Algorithms from Artificial Intelligence: A Modern Approach by Russell and Norvig. 
    
## Applications

  - Natural Language Processing (NLP)
    - **chatter** [![Hackage](https://img.shields.io/hackage/v/chatter.svg)](https://hackage.haskell.org/package/chatter)  [![chatter](http://stackage.org/package/chatter/badge/nightly)](http://stackage.org/nightly/package/chatter) : chatter is a collection of simple Natural Language Processing algorithms, which also comes with models for POS tagging and Phrasal Chunking that have been trained on the Brown corpus (POS only) and the Conll2000 corpus (POS and Chunking).
Chatter supports:
      - Part of speech tagging with Averaged Perceptrons. Based on the Python implementation by Matthew Honnibal: (http://honnibal.wordpress.com/2013/09/11/a-good-part-of-speechpos-tagger-in-about-200-lines-of-python/) See NLP.POS for the details of part-of-speech tagging with chatter.
      - Phrasal Chunking (also with an Averaged Perceptron) to identify arbitrary chunks based on training data.
      - Document similarity; A cosine-based similarity measure, and TF-IDF calculations, are available in the NLP.Similarity.VectorSim module.
      - Information Extraction patterns via (http://www.haskell.org/haskellwiki/Parsec/) Parsec
    - **snowball** [![Hackage](https://img.shields.io/hackage/v/snowball.svg)](https://hackage.haskell.org/package/snowball)  [![chatter](http://stackage.org/package/snowball/badge/nightly)](http://stackage.org/nightly/package/snowball) : The Snowball FFI binding library is used to compute the stems of words in natural languages.
Compared to the older stemmer package, this one:
    - Correctly handles unicode without relying on the system locale
    - Takes greater care to avoid memory leaks and to be thread safe
    - Uses Text rather than String
  - Bioinformatics
    - **NGLess** [](https://github.com/luispedro/ngless){:.github} [![Hackage](https://img.shields.io/hackage/v/ngless.svg)](https://hackage.haskell.org/package/ngless)  [![ngless](http://stackage.org/package/ngless/badge/nightly)](http://stackage.org/nightly/package/ngless) : Ngless is a domain-specific language for NGS (next-generation sequencing data) processing ("NGS with less work").


    

## Datasets

- **datasets** [](https://github.com/DataHaskell/dh-core){:.github} [![Hackage](https://img.shields.io/hackage/v/datasets.svg)](https://hackage.haskell.org/package/datasets)  [![datasets](http://stackage.org/package/datasets/badge/nightly)](http://stackage.org/nightly/package/datasets) : Classical machine learning and statistics datasets from the UCI Machine Learning Repository and other sources.
The datasets package defines two different kinds of datasets: 
  - Small data sets which are directly (or indirectly with file-embed) embedded in the package as pure values and do not require network or IO to download the data set. This includes **Iris**, **Anscombe** and **OldFaithful**
  - Other data sets which need to be fetched over the network and are cached in a local temporary directory.
  Currently maintained within the scope of the [DataHaskell `dh-core` project](https://github.com/datahaskell/dh-core).
- **mnist-idx** [](https://github.com/kryoxide/mnist-idx){:.github} [![Hackage](https://img.shields.io/hackage/v/mnist-idx.svg)](https://hackage.haskell.org/package/mnist-idx)  [![mnist-idx](http://stackage.org/package/mnist-idx/badge/nightly)](http://stackage.org/nightly/package/mnist-idx) : Read and write data in the IDX format used in e.g. the MINST database.

## Language interop

### R

- HaskellR (https://tweag.github.io/HaskellR/)
  - **inline-r** [![Hackage](https://img.shields.io/hackage/v/inline-r.svg)](https://hackage.haskell.org/package/inline-r)  [![inline-r](http://stackage.org/package/inline-r/badge/nightly)](http://stackage.org/nightly/package/inline-r) : Seamlessly call R from Haskell and vice versa. No FFI required. Efficiently mix Haskell and R code in the same source file using quasiquotation. R code is designed to be evaluated using an instance of the R interpreter embedded in the binary, with no marshalling costs and hence little to no overhead when communicating values back to Haskell.
  - **H** [![Hackage](https://img.shields.io/hackage/v/H.svg)](https://hackage.haskell.org/package/H)  [![H](http://stackage.org/package/H/badge/nightly)](http://stackage.org/nightly/package/H) : An interactive prompt for exploring and graphing data sets. This is a thin wrapper around GHCi, with the full power of an R prompt, and the full power of Haskell prompt: you can enter expressions of either language, providing you with plotting and distributed computing facilities out-of-the-box.




## Data science frameworks

### Apache Spark bindings

- **sparkle** [![Hackage](https://img.shields.io/hackage/v/sparkle.svg)](https://hackage.haskell.org/package/sparkle)  [![sparkle](http://stackage.org/package/sparkle/badge/nightly)](http://stackage.org/nightly/package/sparkle) : A library for writing resilient analytics applications in Haskell that scale to thousands of nodes, using Spark and the rest of the Apache ecosystem under the hood.
See the [blog post](https://www.tweag.io/posts/2016-02-25-hello-sparkle.html) for details.

- **distributed-dataset** [](https://github.com/utdemir/distributed-dataset){:.github} [![Hackage](https://img.shields.io/hackage/v/distributed-dataset.svg)](https://hackage.haskell.org/package/distributed-dataset)  [![distributed-dataset](http://stackage.org/package/distributed-dataset/badge/nightly)](http://stackage.org/nightly/package/distributed-dataset) : A distributed data processing framework in pure Haskell. Inspired by Apache Spark.
`Control.Distributed.Dataset` provides a type which lets you express transformations on a distributed multiset. Its API is highly inspired by Apache Spark.
It uses pluggable ShuffleStore's for storing intermediate compuation results. See 'distributed-dataset-aws' for an implementation using S3.
`Control.Distributed.Fork` contains a fork function which lets you run arbitrary IO actions on remote machines; leveraging StaticPointers language extension and distributed-closure library.
This module is useful when your task is embarrassingly parallel:
It uses pluggable Backends for spawning executors. See 'distributed-dataset-aws' for an implementation using AWS Lambda .

- **kraps-h** [](https://github.com/krapsh/kraps-haskell){:.github} [![Hackage](https://img.shields.io/hackage/v/kraps-h.svg)](https://hackage.haskell.org/package/kraps-h)  [![kraps-h](http://stackage.org/package/kraps-h/badge/nightly)](http://stackage.org/nightly/package/kraps-h) : Haskell bindings to Apache Spark. The library consists of: 
  - A specification to describe data pipelines in a language-agnostic manner, and a communication protocol to submit these pipelines to Spark. 
  - A serving library, called krapsh-server, that implements this specification on top of Spark. It is written in Scala and is loaded as a standard Spark package.
  - A client written in Haskell that sends pipelines to Spark for execution. In addition, this client serves as an experimental platform for whole-program optimization and verification, as well as compiler-enforced type checking.


# Contribute

If you know a library that has to do with Data Science, please consider [adding](https://github.com/DataHaskell/docs/edit/gh-pages/_posts/2016-10-19-current-environment.md) it, if the category it belongs to doesn't exist, suggest a category for it.

Add sections related to data science and not only Machine Learning such as Data Mining, Distributed Processing, etc
