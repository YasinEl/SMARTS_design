# SMARTS Design

A toolkit for designing and working with chemical SMARTS patterns using RDKit.

## Overview

This repository provides tools and notebooks for creating, visualizing, and analyzing SMARTS (SMiles ARbitrary Target Specification) patterns, which are used for substructure matching in chemical informatics.

## Setup

### Prerequisites
- Anaconda or Miniconda

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/YasinEl/SMARTS_design.git
   cd SMARTS_design
   ```

2. Create the conda environment:
   ```bash
   conda env create -f requirements.yml
   ```

3. Activate the environment:
   ```bash
   conda activate smarts_design
   ```

4. Start Jupyter:
   ```bash
   jupyter notebook
   ```

## Features

### Molecule Visualization with Atom Numbers

The `code/molecule_visualization.ipynb` notebook provides functionality to:
- Display chemical structures with atom indices for all non-hydrogen atoms
- Visualize molecules from SMILES strings or RDKit molecule objects
- Highlight specific atoms of interest
- Extract detailed atom information (symbol, degree, valence, hybridization, etc.)

This is particularly useful when designing SMARTS patterns, as you need to know the atom indices to reference specific atoms in your patterns.

## Repository Structure

```
SMARTS_design/
├── requirements.yml              # Conda environment file
├── code/                        # Code and notebooks
│   ├── molecule_visualization.ipynb  # Notebook for visualizing molecules with atom numbers
│   └── README.md               # Documentation for code directory
└── README.md                   # This file
```

## Usage Example

```python
from rdkit import Chem
from code.molecule_visualization import display_molecule_with_atom_numbers

# Display a molecule with atom numbers
display_molecule_with_atom_numbers('CCO')  # Ethanol

# Display benzene with custom size
display_molecule_with_atom_numbers('c1ccccc1', size=(600, 600))

# Highlight specific atoms
mol = Chem.MolFromSmiles('CC(=O)O')  # Acetic acid
display_molecule_with_atom_numbers(mol, highlight_atoms=[1, 2])
```

## Dependencies

Main dependencies include:
- **RDKit**: Core chemistry library for molecule manipulation and visualization
- **Jupyter/JupyterLab**: Interactive notebook environment
- **NumPy/Pandas**: Data manipulation
- **Matplotlib/Seaborn**: Visualization
- **Pillow**: Image processing

See `requirements.yml` for the complete list of dependencies.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is open source and available under the MIT License.