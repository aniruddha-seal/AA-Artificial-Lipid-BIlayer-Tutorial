# Lipid Bilayer Water Removal Scripts

## Scripts Overview

1. **`1_Find Z_Max, Z_Min Headgroup P.ipynb`**  
   This script identifies the highest and lowest Z coordinates of the phosphorus (P) headgroup atoms in each leaflet of the bilayer, helping to establish the Z limits of the bilayer.

2. **`2_Select_Water_ZCutoff.ipynb`**  
   This script removes water molecules that are positioned between the defined Z-coordinate limits of the bilayer (identified using the previous notebook). The approach provides an approximation of water removal from within the lipid bilayer chains.

## Usage

- **Requirements**: These scripts are designed for systems prepared in **GROMACS** with water molecules labeled as `SOL` and oxygen atoms labeled as `OW`.
- **Assumptions**: The lipid bilayer should be oriented normal to the Z-axis for accurate application.
  
### Workflow

1. **Step 1**: After solvating your bilayer system, use `1_Find Z_Max, Z_Min Headgroup P.ipynb` to determine the highest and lowest Z-coordinate values of the P headgroup atoms. This will help establish the Z-coordinate limits for water removal.
  
2. **Step 2**: Apply `2_Select_Water_ZCutoff.ipynb` to remove water molecules located between these Z-coordinate limits.
