
# Computer Science - Math - Neural Networks 
<a href='https://github.com/nelson-n/cs-math-nn/blob/main/Assorted/Assets/RepoLogo.png'><img src='/Assorted/Assets/RepoLogo.png' align="right" height="160" /></a>

This curriculum is my personal approach to learning topics in computer science, mathematics, and neural networks (+ quant finance, just for fun) from first principles. This repository is not necessarily a full curriculum, but rather a reflection of my interests, needs, and gaps in my knowledge. However, my goal is to build a curriculum that covers the whole compute stack from transistors and assembly to the math underpinning neural networks. As such, the lessons I compile below should form a solid computer science, math, and deep learning curriculum.

## Sections

* [Hardware / Processors](#hardware--processors)
* [Compilers / Operating Systems](#compilers--operating-systems)
* [Data Structures / Algorithms](#data-structures--algorithms)
* [Computer Languages](#computer-languages)
* [Statistics](#statistics)
* [Mathematics](#mathematics)
* [Neural Networks](#neural-networks)
* [Quantitative Finance](#quantitative-finance)
* [Additional Topics](#additional-topics)
    * [Networking / Internet](#networking--internet)
    * [Parallel Computing](#parallel-computing)
    * [Databases](#databases)
    * [Cryptography](#cryptography) 
    * [Information Theory / Entropy](#information-theory--entropy)
* [Assorted](#assorted)

## Language Cheatsheets
* [Unix Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/CompilersOperatingSystems/Unix/UnixCheatsheet.md)
* [Git Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/Assorted/GitCheatsheet.md)
* [Python Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/Python/PythonCheatsheet.py)
* [R Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/R/RCheatsheet.R)
* [R Plots and Tables Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/R/PlotsTables.R)
* [Java Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/Java/JavaCheatsheet.java)

## Subject Notes
* [General Math Notes](https://github.com/nelson-n/cs-math-nn/blob/main/Math/MathNotes.ipynb)
* [Linear Algebra Notes](https://github.com/nelson-n/cs-math-nn/blob/main/Math/LinearAlgebra.ipynb)
* [Quantitative Finance Notes](https://github.com/nelson-n/cs-math-nn/blob/main/QuantitativeFinance/QuantFinance.ipynb)

## General Cheatsheets
* [Time Complexity Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/DataStructuresAlgorithms/TimeComplexityCheatsheet.md)
* [Data Structures Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/DataStructuresAlgorithms/DataStructuresCheatsheet.md)
* [Programming Paradigms Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/ProgrammingParadigms.md)
* [Binary Trees Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/DataStructuresAlgorithms/BinaryTreeCheatsheet.java)
* [Math Symbols Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/Math/MathSymbolsCheatsheet.md)
* [Equations Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/Assorted/EquationsCheatsheet.md)

## Preface: Atoms to Bits 

`/Assorted/atoms2bits.pdf`

* This preface ([atoms2bits]()) gives an overview of the complete compute stack: the refining of sand into silicon ingots, the doping of silicon to create differences in valence shell electrons, how doped silicon is used to build transistors, how transistors form logic gates, CPU architecture and operation, memory caches, instruction set architecture, operating systems, and higher level languages. This preface gives an overview of concepts that will be covered in detail in later sections of `cs-math-nn`.

#### :bangbang: to-do
* In atoms2bits add notes on FPGAs, how FPGAs are built from transistors, notes on how ICs are a collection of transistors in a reliable package, notes on LUTs (lookup tables).

## Hardware / Processors

#### :bangbang: to-do
* Implement AND, NAND, XOR, and other logic gates from scratch, use these logic gates to build functional units such as a 1-bit adder, multiplexer, sequential logic, SRAM, etc. Use logic gates to create simple implementations of various memory units: L1 cache, DRAM, etc. The functional units built in this section will be used later when building a model instruction set.
* Build a simple ARM7 CPU in Verilog or with another infrastructure.
    * Start by building a pipeline with simple start, decode, fetch, and exectute commands. Then build a simple register/memory unit to push and pull data, a simple ALU (arithmetic logic unit) that can perform basic arithmetic and logic operations, and a simple CU (control unit) for finding instructions and directing operations. These should be built on top of the functional units constructed in the hardware lesson. 
    * Additional: Write basic arithmetic instructions, branch instructions, and memory instructions. Allow for instruction out-of-order, basic parallelism, use dependency graphs for instructions. Set up a memory hierarchy with Registers, L1 cache, L2 cache, L3 cache, and DRAM.
* Extra-curricular: Build a UART in Verilog, GPU basics.

## Compilers / Operating Systems

`/CompilersOperatingSystems`

* Notes on Unix/Linux and a [Unix Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/CompilersOperatingSystems/Unix/UnixCheatsheet.md) of useful commands.

#### :bangbang: to-do
* Create a set of general notes on linux/unix, combine with notes in unix.pdf in local. Add notes on the basic linux filesystem format from [here](https://www.linuxfoundation.org/blog/blog/classic-sysadmin-the-linux-filesystem-explained).
* Build a C compiler in Haskell. Consider the basics of compiler design, write a parser, output ARM assembly which can then be run through the simple processor designed in the processors lesson.
    * Build functions for converting binary to numbers and ASCII characters.
* Learn RISC-V architecture, contrast with x86, ARM, and other instruction set architectures.
* Build a UNIX-ish operating system in C or C++ with simple abilities like open, read, write, close, init, cat, ls, rm.
* Build a filesystem like FAT in C or C++.

## Data Structures / Algorithms

`/DataStructuresAlgorithms`

* Notes and exercises on data structures and algorithms implemented in Java and Python.
* Notes on:
    - Linked lists, queues, stacks, and sets.
    - Sorting and searching algorithms.
    - Hash tables, trees, heaps, and priority queues.
    - Graphs and graph algorithms.
    - [Binary Tree Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/DataStructuresAlgorithms/BinaryTreeCheatsheet.java) covering binary tree search, recursion, and implementation.
* Exercises:
    - Comparison of the speed of recursion in Python, R, Java, C, and C++.

#### :bangbang: to-do
* Learn the low-level data structures behind the base data types in Python such as: list, array, tuple, et cetera. Build versions of these data types in C++ and then port to Python with a package like `pybind11`.
* Add a lesson on the properties of different number systems: hexadecimal system, 32-bit numbers, 128-bit numbers, how with a 32-bit number system you can generate the numbers 0-65535, etc.

## Computer Languages

`/ComputerLanguages`

* Notes, exercises, and cheatsheets on both high level and low level programming languages.
* Notes from popular books such as *Fluent Python*, *Advanced R*, and *Java: A Beginner's Guide*.

Languages currently covered:
* Python - [Python Notes](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/Python/FluentPython.py)
* Java - [Java Notes](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/Java/JavaNotes.java)
* R - [R Notes](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/R/AdvancedR.R)
* Julia - [Julia Notes](https://github.com/nelson-n/cs-math-nn/blob/main/ComputerLanguages/Julia/JuliaNotes.jl)

#### :bangbang: to-do
* Add notes on C, C++, potentially Go or Rust.
* Replicate lower level Python functions such as len(), dictionary, hash table, a sorting algorithm, slicing, indexing, set inclusion, et cetera in C++ to learn how these functions work. Then port these functions to Python with `pybind11`. Interface these functions with the data structures built from scratch in the data structures lesson.
* Overview of object-oriented-programming (OOP).
* Build a dictionary method using C++ and an R dictionary interface. Then publish an R dictionary class to CRAN.

## Statistics

`/Statistics`

* Implements Maximum Likelihood Estimation (MLE) from scratch, then benchmarks against a canonical optimization function.
* Implements the Metropolis-Hastings method from scratch.
* Estimates Ordinary Least Squares (OLS) regression coefficients using Stochastic Gradient Descent (SGD) and tests the accuracy of estimated coefficients out-of-sample.

#### :bangbang: to-do
* Poker exercises: implement a card deck class with operations such as draw X cards, calculate probabilites of different hands given different stages of a game, implement riffle shuffle, et cetera.
* Do some statistics work in Julia.

## Mathematics

`/Math`

* Topics in linear algebra: [Linear Algebra Notes](https://github.com/nelson-n/cs-math-nn/blob/main/Math/LinearAlgebra.ipynb) 
* Topics in calculus: [Calculus Notes](https://github.com/nelson-n/cs-math-nn/blob/main/Math/Calculus.ipynb) 
* Assorted topics in math: [Math Notes](https://github.com/nelson-n/cs-math-nn/blob/main/Math/MathNotes.ipynb) 
* Implements Singular Value Decomposition (SVD) and Principal Component Analysis (PCA) from theory. Uses SVD and PCA to compress images and find the properties of transformed Gaussian data.

#### :bangbang: to-do
* Learn: differential equations, partial differential equations. Work on these problems in Julia or Python.
    * Use 3B1B videos for this.
* Learn: Markov chains, Brownian motion, geometric Brownian motion.
* Review multivariable calculus, gradient descent, formalize pre-existing notes and upload them.

## Neural Networks

`/NeuralNetworks`

* Implements the following neural network architectures from scratch using NumPy and then trains and tests the neural networks out-of-sample.
    * Feedforward Neural Network
    * Recurrent Neural Network
* Solves simple neural network problems relating to finding optimas, gradient descent, et cetera.

#### :bangbang: to-do
* Build the following models from scratch in NumPy: Feedforward neural network -> recurrent neural network -> convolution neural network -> ResNet -> Transformer -> Diffusion Model, all from scratch. 
    * Verify the correct order of the models so that all paradigmatic neural network models are built in-order.

## Quantitative Finance

`/QuantitativeFinance`

* General notes on quantitative finance including:
    * Sensitivity measures and derivations.
    * Yield curve estimation.

## Additional Topics

### Networking / Internet

`/NetworkingInternet`

* Notes on computer networking and how the internet protocol stack works.

#### :bangbang: to-do
* Manually create and send TCP/IP packets: [tutorial](https://inc0x0.com/tcp-ip-packets-introduction/tcp-ip-packets-3-manually-create-and-send-raw-tcp-ip-packets/)

### Parallel Computing 

### Databases

### Cryptography

#### :bangbang: to-do
* Write a hashing function from scratch. Use the hashing function to build a hash table function. 
* Upload pre-existing crptography notes.
* Write a script to generate public/private key pairs using SHA256 or another hashing function.

### Information Theory / Entropy

## Assorted

`/Assorted/GitCheatsheet.md`

* [Git Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/Assorted/GitCheatsheet.md) of useful commands for working with Git and GitHub.

`/Assorted/EquationsCheetsheet.md` 

* [Equations Cheatsheet](https://github.com/nelson-n/cs-math-nn/blob/main/Assorted/EquationsCheatsheet.md) of math, stats, and neural network equations implemented in LaTeX.

## Acknowledgements

[Self-learning-Computer-Science - PKUFlyingPig](https://github.com/PKUFlyingPig/Self-learning-Computer-Science/blob/main/README.md)
Open-source CS curriculum that inspired the structure and content of this curriculum.

[From the Transistor to the Web Browser - George Hotz](https://github.com/geohot/fromthetransistor)
Proposed CS curriculum that inspired many of the low-level CS lessons on computer hardware, chips, and compilers that are in this curriculum.

## To-Do List

* Work on `/Math` calculus fundamentals notes and `/Statistics` statistics fundamentals notes. 
* Add `/QuantitativeFinance` notes on Merton (1974), Nelson-Siegel, Black-Scholes, and a Normal Jump Diffusion Model (GBM that allows for Poisson jumps in asset prices, see Merton 1976).
* Add a quick study of BLAS and LAPACK routines.
    * https://docs.julialang.org/en/v1/stdlib/LinearAlgebra/#BLAS-functions
* Neural Network work.
    * Look at Karpathy lectures.
    * Look at tinygrad tutorial, play with tinygrad.
    * Build paradigmatic models in sequential order up to the Transformer model.
    * Read *Attention Is All You Need* paper.
* Work on *Fluent Python* notes.
* Add LaTeX equations to pre-existing math/stats/neural network exercises and `/Assorted/EquationsCheetsheet.md` based off of this [tutorial](https://blmoistawinde.github.io/ml_equations_latex/#negative-loglikelihood).
* Work on poker exercises.
* Build a hashing function (SHA256) from scratch, then use it to build a hash table class from scratch.
