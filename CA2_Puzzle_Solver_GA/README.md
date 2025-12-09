# 🧩 Genetic Algorithm Puzzle Solver

This project implements a Genetic Algorithm (GA)–based approach for solving a shuffled image puzzle. Each possible puzzle arrangement is represented as a chromosome, and evolutionary techniques are used to search for the correct configuration.

---

## 🚀 Overview

The pipeline begins by splitting an input image into a set of shuffled puzzle pieces. Each piece has four edges, and the goal is to reconstruct the original image by placing all pieces in their correct positions.

To guide the GA, the project defines a fitness function based on the edge compatibility between neighboring pieces. The better two edges align, the higher the score contributed to the chromosome. Over generations, the algorithm attempts to improve the overall fitness of the population.

---

## 🧬 Genetic Algorithm Workflow

### 1. Initial Population  
Random puzzle configurations are generated to form the first population.

### 2. Fitness Evaluation  
Each chromosome is scored using an edge-matching–based fitness function.

### 3. Selection  
High-fitness chromosomes are chosen as parents for the next generation.

### 4. Crossover  
Parents exchange segments to produce new offspring.

### 5. Mutation  
Random modifications (e.g., swapping puzzle pieces) introduce diversity into the population.

### 6. Next Generation  
A new population is formed, and the evolutionary cycle continues.

At the end of the process, the chromosome with the **highest fitness** in the final generation is selected as the predicted solution to the puzzle.

---

## ⚠ Current Challenges

During experimentation, the GA frequently became trapped in **local minima**.  
Even after applying **Bayesian Optimization** to tune hyperparameters such as mutation rate, crossover probability, and population size, the model often plateaued after only one or two generations.  

Improving the algorithm’s ability to escape local minima remains an open challenge and a key direction for future development.

---

## 📌 Project Status

This implementation provides a functional GA-based solver but still requires improvements to reliably avoid local minima and achieve consistent puzzle reconstruction.

---

