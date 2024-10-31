Disclaimer - This project is a three-way collaborative venture undertaken by ChatGPT, Claude AI, and myself. Each party contributed equally to the solution, working together efficiently to create this implementation.

# The Super Parameter Challenge Solution

This repository contains a solution to **The Super Parameter** challenge from the QHack 2023 Flashback Badge Challenge event. The challenge involves constructing a quantum model that, with only one parameter, can generate all computational basis states of a 3-qubit system.

## Description

Within Quantum Machine Learning (QML), expressivity refers to the range of models that can be represented by varying parameters within an ansatz. This challenge pushes the concept to its limits by requiring a single-parameter model capable of producing all 8 computational basis states of a 3-qubit system.

Our solution uses the `np.heaviside` function in combination with sine functions to create smooth transitions between the basis states as the parameter `alpha` varies within the interval [0, 10]. The model ensures continuity, and the specific `alpha` values corresponding to each basis state are provided.

## Files

- `main.py`: Contains the implementation of the `model` and `generate_coefficients` functions.
- `LICENSE`: MIT License under which this project is distributed.

## Requirements

- Python 3.x
- PennyLane
- NumPy

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/super-parameter-challenge.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd super-parameter-challenge
   ```

3. **Install the required packages**:

   ```bash
   pip install pennylane numpy
   ```

## Usage

Run the `main.py` script to test the solution:

```bash
python main.py
```

This will execute the `test_solution` function, which prints the probabilities for each computational basis state generated by the model at specific `alpha` values.

## Example Output

```
Alpha: 8.750, State: |000⟩, Probabilities: [1. 0. 0. 0. 0. 0. 0. 0.]
Alpha: 7.500, State: |001⟩, Probabilities: [0. 1. 0. 0. 0. 0. 0. 0.]
Alpha: 5.000, State: |010⟩, Probabilities: [0. 0. 1. 0. 0. 0. 0. 0.]
Alpha: 6.250, State: |011⟩, Probabilities: [0. 0. 0. 1. 0. 0. 0. 0.]
Alpha: 1.250, State: |100⟩, Probabilities: [0. 0. 0. 0. 1. 0. 0. 0.]
Alpha: 0.000, State: |101⟩, Probabilities: [0. 0. 0. 0. 0. 1. 0. 0.]
Alpha: 2.500, State: |110⟩, Probabilities: [0. 0. 0. 0. 0. 0. 1. 0.]
Alpha: 3.750, State: |111⟩, Probabilities: [0. 0. 0. 0. 0. 0. 0. 1.]
```

## Project Structure

- **`model(alpha)`**: A quantum function that takes a single parameter `alpha` and returns the probability vector of the resulting quantum state. It uses rotation gates and optional entanglement to generate the basis states.
- **`generate_coefficients()`**: Generates a list of 8 specific `alpha` values that correspond to each computational basis state.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributors

This solution was developed collaboratively by:

- Jon Poplett
- ChatGPT
- Claude

## Acknowledgments

- **QHack 2023**: For presenting this engaging and challenging problem.
- **PennyLane**: For providing the tools necessary for quantum computing simulations.

## Contact

For questions or feedback, please open an issue in this repository or contact JonPoplet@JGPTech.net. 

```
