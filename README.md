Ipopt
=====

Introduction
------------

Ipopt (Interior Point OPTimizer, pronounced eye-pea-Opt) is a software package for large-scale [nonlinear optimization](http://wiki.mcs.anl.gov/NEOS/index.php/Nonlinear_Programming_FAQ).
It is designed to find (local) solutions of mathematical optimization problems of the form

```
   min     f(x)
  x ∈ Rⁿ

s.t.       g_L ≤ g(x) ≤ g_U
           x_L ≤  x   ≤ x_U
```
where ```f(x): Rⁿ --> R``` is the objective function, and ```g(x): Rⁿ --> Rᵐ```
are the constraint functions.  The vectors `g_L` and `g_U` denote the lower and upper bounds on the constraints, and the vectors `x_L` and `x_U` are the bounds on the variables `x`.
The functions `f(x)` and `g(x)` can be nonlinear and nonconvex, but should be twice continuously differentiable.
Note that equality constraints can be formulated in the above formulation by setting the corresponding components of `g_L` and `g_U` to the same value.

Ipopt is part of the [COIN-OR Initiative](http://www.coin-or.org).

Background
----------

Ipopt is written in C++ and is released as open source code under the Eclipse Public License (EPL).
The code has been written by [Andreas Wächter](http://www.mccormick.northwestern.edu/directory/profiles/Andreas-Waechter.html) and [Carl Laird](http://allthingsoptimal.com/biography/).
The COIN-OR project managers for Ipopt are [Andreas Wächter](http://users.iems.northwestern.edu/~andreasw) und [Stefan Vigerske](https://www.gams.com/~stefan).
For a list of **all contributors**, see the [AUTHORS file](Ipopt/AUTHORS).

The C++ version has first been [released on Aug 26, 2005](http://list.coin-or.org/pipermail/ipopt/2005-August/000331.html) as version 3.0.0.
The previously released [pre-3.0 Fortran version](http://www.coin-or.org/Ipopt/ipopt-fortran.html) is no longer maintained.


The Ipopt distribution can be used to generate a library that can be linked to one's own C++, C, Fortran, or Java code, as well as a solver executable for the [AMPL](http://www.ampl.com) modeling environment.
The package includes interfaces to [CUTEr](http://cuter.rl.ac.uk/cuter-www/) optimization testing environment, as well as the [MATLAB](http://www.mathworks.com/products/matlab) and [R](http://www.r-project.org/) programming environments.
IPOPT can be used on Linux/UNIX, Mac OS X and Windows platforms.

As open source software, the source code for Ipopt is provided without charge.
You are free to use it, also for commercial purposes.
You are also free to modify the source code (with the restriction that you need to make your changes public if you decide to distribute your version in any way, e.g. as an executable); for details see the EPL license.
And we are certainly very keen on feedback from users, including contributions!

In order to compile Ipopt, certain third party code is required (such as some linear algebra routines).
Those are available under different conditions/licenses.

If you want to learn more about Ipopt, you can find references in the [bibliography of the documentation](http://www.coin-or.org/Ipopt/documentation/node64.html) and this ["Papers about Ipopt" page](https://projects.coin-or.org/Ipopt/wiki/IpoptPapers).

For information on projects that use Ipopt, refer to the [Success Stories page](https://projects.coin-or.org/Ipopt/wiki/SuccessStories).


Download
--------

**[Download Ipopt source as tarballs.](http://www.coin-or.org/download/source/Ipopt)**

You can also obtain the Ipopt code via Git.
Please refer to the [documentation](http://www.coin-or.org/Ipopt/documentation/) and the [General Configuration and Installation Instructions for COIN-OR projects](https://projects.coin-or.org/CoinHelp/).

**Please make sure you read the [current issues page](https://projects.coin-or.org/CoinHelp/wiki/current-issues) before you try to install Ipopt.**

Also still available is the no longer maintained older [Fortran version](http://www.coin-or.org/Ipopt/ipopt-fortran.html).

Additionally, **[JuliaOpt provides Ipopt binaries](https://github.com/JuliaOpt/IpoptBuilder/releases)**,
**[AMPL provides binaries](http://ampl.com/products/solvers/open-source/#ipopt)** for using Ipopt through AMPL,
and the **[Pardiso project provides binaries](https://pardiso-project.org/index.html#binaries)** for using Ipopt with Pardiso through Matlab.


Documentation and Support
-------------------------

The [main Ipopt documentation](http://www.coin-or.org/Ipopt/documentation/) contains
 * **[Installation Instructions](http://www.coin-or.org/Ipopt/documentation/node10.html)**
   * [Getting Ipopt code](http://www.coin-or.org/Ipopt/documentation/node12.html) and [3rd party code](http://www.coin-or.org/Ipopt/documentation/node13.html)
   * **[Compiling Ipopt](http://www.coin-or.org/Ipopt/documentation/node14.html)** ([under Windows](http://www.coin-or.org/Ipopt/documentation/node15.html))
   * **[Java Interface](http://www.coin-or.org/Ipopt/documentation/node16.html)**
   * **[R Interface](http://www.coin-or.org/Ipopt/documentation/node17.html)**
   * **[MATLAB Interface](http://www.coin-or.org/Ipopt/documentation/node18.html)**
   * [Expert Installation Options](http://www.coin-or.org/Ipopt/documentation/node19.html)
 * **[Interfacing Ipopt](http://www.coin-or.org/Ipopt/documentation/node20.html)**
   * [AMPL](http://www.coin-or.org/Ipopt/documentation/node21.html)
   * [Code](http://www.coin-or.org/Ipopt/documentation/node22.html):
     [C++](http://www.coin-or.org/Ipopt/documentation/node23.html),
     [C](http://www.coin-or.org/Ipopt/documentation/node24.html),
     [Fortran](http://www.coin-or.org/Ipopt/documentation/node25.html),
     [Java](http://www.coin-or.org/Ipopt/documentation/node26.html)
   * [R](http://www.coin-or.org/Ipopt/documentation/node27.html)
   * [MATLAB](http://www.coin-or.org/Ipopt/documentation/node28.html)
 * **Special Features**:
   * [Derivative Checker](http://www.coin-or.org/Ipopt/documentation/node30.html)
   * [Hessian Approximation](http://www.coin-or.org/Ipopt/documentation/node31.html)
   * [Warm starts via AMPL](http://www.coin-or.org/Ipopt/documentation/node32.html)
   * [sIpopt: Optimal Sensitivity Based on AMPL/Ipopt](http://www.coin-or.org/Ipopt/documentation/node33.html)
 * **[Output](http://www.coin-or.org/Ipopt/documentation/node36.html)**
 * [Option Files](http://www.coin-or.org/Ipopt/documentation/node35.html),
   **[Options Reference](http://www.coin-or.org/Ipopt/documentation/node40.html)**, [Options available via AMPL](http://www.coin-or.org/Ipopt/documentation/node63.html)

Further Information:
 * **[FAQ](https://projects.coin-or.org/Ipopt/wiki/FAQ)** (Frequently Asked Questions)
 * **[Mailing list archive](http://list.coin-or.org/pipermail/ipopt/)**
 * **[Compilation hints](https://projects.coin-or.org/Ipopt/wiki/CompilationHints)** collected by users (partly outdated)
 * **[Current configuration and installation issues](https://projects.coin-or.org/CoinHelp/wiki/current-issues)** for COIN-OR projects
 * [General Configuration and Installation Instructions](https://projects.coin-or.org/CoinHelp/) for COIN-OR projects
 * [short Ipopt tutorial](http://drops.dagstuhl.de/volltexte/2009/2089/pdf/09061.WaechterAndreas.Paper.2089.pdf)
 * [Hints and tricks](https://projects.coin-or.org/Ipopt/wiki/HintsAndTricks) on using Ipopt
 * [Doxygen documentation for the Ipopt source code](http://www.coin-or.org/Ipopt/doxygen) can be generated by executing `make doxydoc` in an Ipopt build directory

Getting Help:
 * **[Mailing list](http://list.coin-or.org/mailman/listinfo/ipopt)**: subscribe to get notifications about updates and to post questions and comments regarding Ipopt
 * **[Issue tracking system](https://github.com/coin-or/Ipopt/issues/)**: If you believe you found a **bug** in the code, please use the issue tracking system.
   Please include as much information as possible, and if possible some (ideally simple) example code so that we can reproduce the error.

Related Projects
----------------

**[COIN-OR/ADOL-C](https://projects.coin-or.org/ADOL-C)**: Using Ipopt via **C++** and automatic differentiation ([examples](https://projects.coin-or.org/ADOL-C/browser/stable/2.4/ADOL-C/examples/additional_examples/ipopt)).

**[COIN-OR/AIMMSlinks](https://projects.coin-or.org/AIMMSlinks)**: Using Ipopt via **AIMMS**

**[COIN-OR/CppAD](https://projects.coin-or.org/CppAD)**: Using Ipopt via **C++** and automatic differentiation ([example](http://www.coin-or.org/CppAD/Doc/ipopt_solve.htm)).

**[COIN-OR/GAMSlinks](https://projects.coin-or.org/GAMSlinks)**: Using Ipopt via **GAMS**

**[COIN-OR/Optimization Services](https://projects.coin-or.org/OS)**: Using Ipopt via  **OS**

**[APMonitor](http://apmonitor.com)**: MATLAB, Python, and Web Interface to Ipopt with **APMonitor** for Android, Linux, Mac OS X, and Windows

**[CasADi](https://github.com/casadi/casadi/wiki)**: Using Ipopt in a symbolic framework for automatic differentiation and numeric optimization.

**[csipopt](https://github.com/cureos/csipopt)**: Interfacing Ipopt from .NET languages such as **C#**, **F#** and **Visual Basic.NET**.

**[ifopt](https://github.com/ethz-adrl/ifopt)**: Modern, light-weight (~1k loc), **Eigen**-based **C++** interface to Ipopt and Snopt   

**[JuMP](https://github.com/JuliaOpt/JuMP.jl)**: Algebraic modeling with automatic differentiation in **Julia** ([low-level interface](https://github.com/JuliaOpt/Ipopt.jl) also available)

**[MADOPT](https://github.com/stanle/madopt)**: Light-weight C++ and Python modelling interfaces implementing expression building using operator overloading and automatic differentiation.

**[mexIPOPT](https://github.com/ebertolazzi/mexIPOPT)**: a rewrite of the **MATLAB** interface that is contained in Ipopt

**[OPTI Toolbox](http://www.i2c2.aut.ac.nz/Wiki/OPTI/)**: Windows x86 + x64 **MATLAB** Interface, including binaries

**[pyipopt](http://code.google.com/p/pyipopt/)**: Interfacing Ipopt from **Python**

**[sci-ipopt](http://forge.scilab.org/index.php/p/sci-ipopt)**: Interfacing Ipopt from **Scilab** (a free MATLAB-like environment)

Please Cite Us
--------------

We provide this program in the hope that it may be useful to others, and we would very much like to hear about your experience with it.
If you found it helpful and are using it within our software, we encourage you to add your feedback to the [Success Stories page](https://projects.coin-or.org/Ipopt/wiki/SuccessStories).

Since a lot of time and effort has gone into Ipopt's development, **please cite the following publication if you are using Ipopt for your own research**:

* A. Wächter and L. T. Biegler, **[On the Implementation of a Primal-Dual Interior Point Filter Line Search Algorithm for Large-Scale Nonlinear Programming](http://dx.doi.org/10.1007/s10107-004-0559-y)**, _Mathematical Programming_ 106(1), pp. 25-57, 2006
  ([preprint](http://www.optimization-online.org/DB_HTML/2004/03/836.html))
