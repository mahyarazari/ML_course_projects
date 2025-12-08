# Jigsaw Puzzle Solver

## Overview
This repository contains a Jupyter Notebook that implements a computational approach to solving square-piece jigsaw puzzles.

The project focuses on defining a robust **local fit score** and using a search strategy (implemented within the notebook) to reconstruct the original image from scrambled pieces.

## Core Methodology
The quality of the fit between two adjacent puzzle pieces is quantified using the **Local Fit Score**. This score is calculated as the **Sum of Squared Differences (SSD)** of the pixel values along the shared edge.

$$
\text{SSD} = \sum_{p \in \text{Edge}} (I_1(p) - I_2(p))^2
$$
The objective is to minimize the total SSD across all adjacent pairs in the final assembly.

## File Structure
* `jigsaw_puzzle_GA.ipynb`: The main Jupyter Notebook containing all the setup, implementation of the fit score, search algorithm, and analysis.

## Requirements
The project requires the following Python libraries:
* `Python 3.x`
* `numpy`
* `Pillow (PIL)`
* `matplotlib`
* `random`
* `itertools`

You can install the necessary packages using pip:
```bash
pip install numpy Pillow matplotlib
