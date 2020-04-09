# Julia Binder demo

This is a demo of Julia functionality for the Binder project. Simply
go to the URL below and it will launch an interactive Julia environment:

This is another Demo:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/binder-examples/demo-julia/master?filepath=demo.ipynb)


This is for the tutorial today:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kurtsansom/demo-julia/master?filepath=julia_demo.ipynb)


# Getting it running locally
If you don't want to use binder getting ot up and running locally uses the following:

## 1. Install Dependencies
* install [julia-1.3+](https://julialang.org/downloads/)
* clone the repo
```
git clone https://github.com/kurtsansom/demo-julia
cd julia_demo
```
* run julia from command line, (Starting the REPL)
```
#OSX
> exec '/Applications/Julia-1.4.app/Contents/Resources/julia/bin/julia'
# linux, if its in the path  or wherever you installed it
> julia
```

## 2. Add Packages
  1. start the julia REPL in the project dir and activate the current dir
  2. from the REPL switch to 'Package Manager Mode' by pressing the ']' key
  ```
  julia> ]
  ```
  3. activate the current directory (creates a new virtual environment)
  ```
  (v1.3) pkg> activate .
  ```
  4. add packages
  ```
  (demo-julia) pkg> add IJulia DataFrames FileIO JSON PlotThemes Plots PyCall PyPlot
  ```
  5. escape pkg using crt+c


## 3. Start IPython
# "detached=true" creates a seperate instance of jupyterlab
```
julia> using IJulia
julia> jupyterlab()
```
A browser should open up with the jupyterlab instance.

## 4. Find notebook and open it from the directory in the browser