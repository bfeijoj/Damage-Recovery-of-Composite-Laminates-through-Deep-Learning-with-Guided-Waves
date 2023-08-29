# Damage Recovery of Composite Laminates through Deep Learning with Guided Waves

Welcome to the repository dedicated to the solution algorithm discussed in the paper titled 'Damage Recovery in Composite Laminates through Deep Learning from Acoustic Scattering of Guided Waves'. Here, we present a comprehensive collection of notebooks that exemplify the methodology proposed in the paper.

**Author:** Bernardo Feijó Junqueira

## Table of Contents

- [Notebooks and Execution Order](#notebooks-and-execution-order)
- [Directory Structure](#directory-structure)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

## Notebooks and Execution Order

1. ### `compute_dispersion_curves.ipynb`
\
    This notebook calculates dispersion curves for both flawless and flawed composite structures. It aids in selecting optimal guided mode parameters.

2. ### `reconstruct_mode_structure.ipynb`
\
    This notebook computes the guided mode structure of a flawless composite (specular part) using parameters chosen from the dispersion curves analysis.

3. ### `solve_acoustic_scattering_problem.ipynb`
\
    This notebook tackles the direct acoustic scattering problem as an optimization task. It provides a step-by-step approach to solving the direct problem.

4. ### `generate_samples.ipynb`
\
    This notebook generates stochastic defect fields and corresponding scattered guided mode responses from the direct problem's solution.

5. ### `training.ipynb`
\
    This notebook trains a deep learning model (multilayer perceptron) to recover interfacial defect fields.

6. ### `predict.ipynb`
\
    This notebook utilizes a pre-trained deep learning model to recover interfacial defect fields from a scattered displacement field response.

## Directory Structure
To execute these scripts seamlessly, adhere to the following directory structure:


```bash
|-- Work Directory
      |
      |-- compute_dispersion_curves.ipynb
      |-- reconstruct_mode_structure.ipynb
      |-- solve_acoustic_scattering_problem.ipynb
      |-- generate_samples.ipynb
      |-- training.ipynb
      |-- predict.ipynb
      |
      |-- data
      |     |
      |     |-- aluminum-copper_zz
      |     |     |
      |     |     |-- damages
      |     |     |-- random_fields
      |     |     |-- residuals
      |     |     |-- scattered_fields
      |     |
      |     |-- copper-stainless steel_xx
      |           |
      |           |-- damages
      |           |-- random_fields
      |           |-- residuals
      |           |-- scattered_fields
      |
      |-- results
            |
            |-- dispersion_curves
            |-- models
            |-- modes_parameters
```

## Getting Started

To explore and work with the provided notebooks, ensure you have the required software and dependencies installed. Clone the repository to your local environment using:

```bash
git clone https://github.com/bfeijoj/Damage-Recovery-of-Composite-Laminates-through-Deep-Learning-with-Guided-Waves.git
```

In order to properly execute the notebooks presented in this repository, please install the python libraries contained in the **'requirements.txt'** with the following:

```bash
pip install -r requirements.txt
```

## Contributing

Contributions to this repository are welcome! Feel free to submit issues and pull requests to enhance the functionality, documentation, or address any bugs.

## License

This project is licensed under the GNU GENERAL PUBLIC License.

:four_leaf_clover: Feel free to explore, execute, and build upon these notebooks to understand and apply the methodology presented in the associated paper.
