# SMARTS Design Code

This directory contains code and notebooks for designing and working with SMARTS patterns.

## Files

- **molecule_visualization.ipynb**: Jupyter notebook with functions to display chemical structures with atom numbers

## Setup

1. Create the conda environment from the root directory:
   ```bash
   conda env create -f requirements.yml
   ```

2. Activate the environment:
   ```bash
   conda activate smarts_design
   ```

3. Start Jupyter:
   ```bash
   jupyter notebook
   ```
   or
   ```bash
   jupyter lab
   ```

4. Open `molecule_visualization.ipynb`

## Key Functions

### `display_molecule_with_atom_numbers(mol_input, size=(400, 400), highlight_atoms=None)`

Displays a chemical structure with atom numbers for all non-hydrogen atoms.

**Parameters:**
- `mol_input`: SMILES string or RDKit molecule object
- `size`: Image size tuple (width, height)
- `highlight_atoms`: List of atom indices to highlight (optional)

**Example:**
```python
# Display ethanol with atom numbers
display_molecule_with_atom_numbers('CCO')

# Display benzene with custom size
display_molecule_with_atom_numbers('c1ccccc1', size=(600, 600))
```

### `get_atom_info(mol_input)`

Returns detailed information about all non-hydrogen atoms in a molecule.

**Example:**
```python
# Get atom information
info = get_atom_info('c1ccccc1')
print(info)
```
