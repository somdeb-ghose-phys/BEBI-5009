# Mathematical Modeling in Systems Biology

![GitHub repo size](https://img.shields.io/github/repo-size/NTUMitoLab/BEBI-5009) ![GitHub commit activity](https://img.shields.io/github/commit-activity/m/NTUMitoLab/BEBI-5009)

> Mathematical Modeling of Systems Biology, MMSB

NBViewer: <https://nbviewer.jupyter.org/github/NTUMitoLab/BEBI-5009/tree/main/>

## Course information

👩‍🏫 Instructor: An-Chi Wei @ MD 521

🦜 Teaching assistant: Wen-Wei Tseng @ MD 705

📝 Announcements & homeworks: [NTU Cool](https://cool.ntu.edu.tw/)

📗 Textbook: Mathematical Modeling in Systems Biology(2013), by Brian P. Ingalls ([pdf](https://www.math.uwaterloo.ca/~bingalls/MMSB/MMSB_w_solutions.pdf), [MATLAB code](https://www.math.uwaterloo.ca/~bingalls/MMSB/MMSB_code.xhtml))

📚 Additional materials
- An Introduction to Stochastic Processes with Applications to Biology ([pdf](http://sistemas.fciencias.unam.mx/~silo/Cursos/coronavirus/Allen.pdf))

## Course content

Chapter 1-4 describes mathematical modelling in molecular systems biology.

- Basic notions of mathematical modelling.
- Dynamic mathematical models of chemical reaction networks. (ODE models)
- Biochemical kinetics of enzyme-catalysed reactions and cooperative binding. 
- Model reductions.
- Analyzing differential equation models: phase plane, stability, bifurcations, sensitivity analysis.

Chapter 5 and beyond are applications in specific biological domain(s).

- Stoichiometric modelling for large-scale metabolic networks. e.g. [CobraPy](https://opencobra.github.io/cobrapy/)
- Signal transduction pathways.
- Gene regulatory networks.
- Electrophysiology and neuronal action potentials.

## Resources to learn Julia

1. [Think Julia](https://benlauwens.github.io/ThinkJulia.jl/latest/book.html)
2. [From zero to Julia](https://techytok.com/from-zero-to-julia/)
3. [Julia cheat sheet](https://juliadocs.github.io/Julia-Cheat-Sheet/) if you are familiar with Python and/or MATLAB.
4. [Official Julia Manual](https://docs.julialang.org/) to look up definitions.
5. [Julia for Pythonistas](https://colab.research.google.com/github/ageron/julia_notebooks/blob/master/Julia_for_Pythonistas.ipynb) Google Colab notebook.
6. [Learn Julia](https://julialang.org/learning/) from the official website.
7. [Introduction to Julia](https://github.com/xorJane/Introduction_to_Julia_tutorials) jupyter notebooks
8. [MIT Julia course for numerical computing](https://github.com/mitmath/julia-mit)
9. [Learn Julia via epidemic modelling](https://github.com/dpsanders/LearnJulia2020)

## Why Julia?

[John F. Gibson's talk](https://github.com/johnfgibson/whyjulia/blob/master/1-whyjulia.ipynb)

- Right tool for this course to solve differential equations and stochastic simulations
- Python/MATLAB-like syntax + natural math presentation
- C-like speed (!) + built-in parallelism
- Composable and extensible (e.g. DiffEq + ANN)

## Caveats about Julia?

- Time to first plot (TTFF). Code needs to be compiled first so it is less responsive than Python. (but much faster afterwards)
- Less libraries in some domains (e.g. metabolic networks) due to smaller ecosystems.
- Arrays start at one.

## Install and run Julia

[Download Julia](https://julialang.org/downloads/) and install.

### REPL workflow

Run the julia REPL (terminal) and start typing, which is good for simple things like 1+1.

### Jupyter workflow

This workflow is suitable for demonstrations, data explorations, and report submissions.

Open the Julia terminal and enter the following commands to install IJulia, the Julia kernel for Jupyter notebooks.

```julia
import Pkg

Pkg.add("IJulia")
```

And then run Jupyter Lab either from the Julia terminal.

```julia
import IJulia

# Will open home directory by default, which is %userprofile% in Windows and `~` in Linux.
IJulia.jupyterlab()  
```

Or open a new launcher and select Julia in Jupyter lab.

### Pluto notebook workflow

[`Pluto.jl`](https://github.com/fonsp/Pluto.jl) is a reactive notebook environment that automatically updates all dependent values when a function or variable is altered.

It is used in the MIT course [Introduction to Computational Thinking](https://computationalthinking.mit.edu/Spring21/). See also [youtube video](https://youtu.be/C4QhZcX34mI) for using `Pluto.jl`.

```julia
import Pkg

Pkg.add("Pluto")

using Pluto

Pluto.run()
```

### VS Code workflow

[VS Code](https://code.visualstudio.com/) with [Julia extension](https://www.julia-vscode.org/) works better for structured code. See this [Youtube video](https://www.youtube.com/watch?v=IdhnP00Y1Ks).

> Another IDE, [Juno](https://junolab.org), entered [in maintenance mode](https://www.youtube.com/watch?v=rQ7D1lXt3GM) in 2020. It is recommended to use VSCode now.

### Google collab

Open this [Julia for Pythonistas](https://colab.research.google.com/github/ageron/julia_notebooks/blob/master/Julia_for_Pythonistas.ipynb) notebook, save a copy to your Google drive, and run it.

You'll need to reload the browser window after the first cell is executed to load the Julia kernel. Also there is no syntax highlighting for Julia in that environment.
