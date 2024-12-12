"Projet Simulation"
# Optimal Stopping Simulation with Bellman, Grid Search, and Optuna

This project implements a simulation-based approach to solving an optimal stopping problem. Using Monte Carlo simulations, the code explores three optimization methods to find the best stopping condition parameter `a` for maximizing the expected ratio between cumulative averages and prices. 

---

## Features

- **Simulation of Price and Average Paths**: Monte Carlo simulation of asset prices and cumulative averages.
- **Optimal Stopping Strategies**:
  - Grid Search
  - Dynamic Programming with Bellman Equation
  - Bayesian Optimization with Optuna
- **Visualization**:
  - Price and average trajectories
  - Optimization history (Optuna)
  - Comparison of expected ratios for Grid Search and Bellman

---

## Dependencies

To run this project, ensure the following Python libraries are installed:

- `numpy`
- `matplotlib`
- `optuna`

You can install them using pip:

```bash
pip install numpy matplotlib optuna
```

---

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/optimal-stopping-simulation.git
cd optimal-stopping-simulation
```

2. Run the script:

```bash
python simulator.py
```

3. Explore the output:

- **Trajectories**: View simulated price and average paths.
- **Optimization Results**: Find the optimal `a` using Grid Search, Bellman, and Optuna.
- **Visualizations**: Compare the performance of optimization methods.

---

## Code Structure

- `Simulator` Class:
  - `simulate_multiple_trajectories()`: Simulates price and average paths.
  - `plot_trajectories()`: Visualizes a single trajectory of price and average paths.
  - `compute_expected_ratio(a)`: Computes the expected ratio for a given stopping parameter.
  - `find_optimal_a_grid_search(a_values)`: Implements grid search to find the optimal `a`.
  - `bellman(S_paths, A_paths, N, a_values)`: Uses dynamic programming to find the optimal `a`.

- `main()` Function:
  - Simulates trajectories and applies optimization methods.
  - Plots and compares results.

---

## Examples

### 1. Simulated Trajectories

The plot shows:
- **S (Price)**: Simulated price paths.
- **A (Average)**: Cumulative averages over time.

### 2. Optimization Results

- **Grid Search**: Exhaustive search over a range of `a` values.
- **Bellman**: Dynamic programming to compute the expected ratio.
- **Optuna**: Bayesian optimization to maximize the expected ratio.

---

## Contributions

Feel free to contribute by opening a pull request or creating an issue. Suggestions for improvements and bug fixes are always welcome.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
