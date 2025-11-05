# Genetic Algorithm from Scratch for Benchmark Optimization

This project implements a Genetic Algorithm (GA) entirely from scratch using Python and NumPy to solve standard global optimization benchmark functions.
The algorithm evolves candidate solutions over multiple generations through selection, crossover, and mutation, aiming to find the minimum values for classic optimization test functions.

Benchmark Functions Used

    Function	Purpose
    Sphere	    Tests convergence on smooth convex surface
    Rosenbrock	Tests ability to navigate narrow curved valleys
    Rastrigin	Tests performance on highly multi-modal landscape

Goal: Minimize each function.

Key Features

Pure Python + NumPy implementation

Tournament selection strategy

Single-point crossover operator

Random mutation for exploration

Custom duplication and population handling logic

Fitness tracking across generations

Log-scale visualization of optimization progress

Genetic Algorithm Flow

    Step	Description
    1	Initialize random population within bounds
    2	Evaluate fitness using selected benchmark function
    3	Tournament selection to choose parents
    4	Single-point crossover to generate children
    5	Random mutation to maintain diversity
    6	Replace population and repeat
    7	Stop early if optimum (≈0) reached
    
Configuration

    Parameter	Value
    Population size	10
    Dimensions	10
    Iterations	10,000
    Search Range	[-100, 100]
    Results (Sample Run)
    Function	Best Fitness Found
    Sphere	~1712.01
    Rosenbrock	~5.12e7
    Rastrigin	~1487.57

Values show basic convergence. Performance can improve with tuned operators, elitism, and adaptive mutation.

Visualization

The algorithm plots log-scaled fitness progress for each benchmark function:

plt.semilogx(...)


This helps visualize convergence trends over time.

How to Run

Requirements

    numpy
    matplotlib
    random (standard Python)

Execution

    python main.py

File Structure

    genetic_algorithm/
    │── GA.py   # Implementation & execution
    │── README.md

Learning Objective

This project demonstrates core evolutionary-algorithm concepts:

Genetic search heuristics

Fitness-based selection

Mutation for exploration

Convergence behavior on different landscapes

Ideal for understanding evolutionary computation fundamentals without external libraries.
