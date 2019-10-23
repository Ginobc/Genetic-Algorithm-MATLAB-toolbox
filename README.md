# Genetic Algorithm (GA) toolbox

## Overview

This GA toolbox is a free software optimization tool that was established with the Colherinhas' master dissertation (Refs/2016_Master_FERRAMENTA DE OTIMIZAÇÃO VIA ALGORITMOS GENÉTICOS COM APLICAÇÕES EM ENGENHARIA.pdf - portuguese version) with the goal of search/ minimize/ maximize a specific fitness function.

## Compiling & Using GA toolbox

### MATLAB
"main.m" file is responsable to run the GA optimization, by defining the optimization parameters (number of generations, chromosomes, decimation step, and the probabilities of decimation, elitism, mutation and crossover).

When main.m file is running will ask for insert a .m function to be minimized. There are four optimization problems inside the folder "examples" (Eason, Hadel, Sphere and a simple function).

By default the GA toolbox minimizes the "xxxx_function" function (defined as "y") for specific lower and upper limits (L_1, L_2, ... and U_1, U_2, ...). To maximize just put (1/y). GA toolbox identifies automatically the bound vector size defined in the vector bounds = [L_1 U_1; L_2 U_2; L_3 U_3].

Inside the folder "fix" there are defined the evolutionary strategies used in the optimization problem (Roullete-Wheel, BLX-alpha, elitism and decimation) and the random new chromosomes of the population.

### Julia

To run the Julia version, first install the dependencies.

`]add JLD, Statistics, LinearAlgebra, Printf, Plots`

By default, the fitness function is defined on the fitness.jl file. The initial population is created using new_pop.jl and the evolution strategies are defined on evolution_strategies.jl. This strategies are decimation, crossover and mutation.

The upper and lower bounds are defined in the variable CromLim in the main function.

## Results & post-processor
When optimization ends, the elapsed time (in seconds) and the optimum results are shown.
An optimization curve is also created showing the evolution of the optimal result and the mean chromosomes.
