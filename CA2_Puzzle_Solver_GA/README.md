🧩 Genetic Algorithm Puzzle Solver

This project implements a Genetic Algorithm (GA)–based method for solving a shuffled image puzzle. The main idea is to treat each possible puzzle arrangement as a chromosome and use evolutionary techniques to search for the correct configuration.

🚀 Overview

The pipeline begins by converting an input image into a set of shuffled puzzle pieces. Each piece has four edges, and the goal is to reconstruct the original image by placing all pieces in their correct positions.

To guide the GA, the project defines a fitness function based on the edge compatibility between adjacent pieces. The better the edges match, the higher the fitness score of the chromosome. Over successive generations, the algorithm attempts to improve the population’s overall fitness.

🧬 Genetic Algorithm Design

The evolutionary process follows the standard GA workflow:

Initial Population
A set of random puzzle arrangements is generated as the initial population.

Fitness Evaluation
Each chromosome is scored according to the alignment quality of neighboring piece edges.

Selection
The best-performing chromosomes serve as parents for the next generation.

Crossover
Parent chromosomes are recombined to produce new offspring with mixed characteristics.

Mutation
Random swaps or modifications are applied to introduce diversity and prevent premature convergence.

Next Generation
A new population is formed, and the cycle repeats.

At the end of the process, the algorithm selects the chromosome with the highest fitness score from the final generation as the predicted puzzle solution.

⚠ Current Challenges

During development, the algorithm frequently became stuck in local minima. Even after applying Bayesian Optimization to tune hyperparameters (population size, mutation rate, crossover probability, etc.), the GA often plateaued after only one or two generations.

Addressing this issue—either through improved fitness modeling, diversity-preserving operators, or alternative search strategies—is the main direction for future work.

🔧 Future Improvements

Planned enhancements include:

More robust mutation strategies

Adaptive or self-tuning evolutionary parameters

Hybrid optimization (GA + simulated annealing / tabu search)

Improved compatibility metrics for puzzle edges

Further exploration of Bayesian Optimization and alternative meta-heuristics
