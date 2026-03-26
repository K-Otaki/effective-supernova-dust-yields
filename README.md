# Dust Yield and Size Distribution Tables (Otaki et al. 2026)

This repository provides dust yield tables and grain size distributions computed in Otaki et al. (2026).

These datasets are designed for studies of dust production in core-collapse supernovae, including the effects of stellar rotation, metallicity, and reverse shock processing.

## 1. Dust Yields

- `DustYield_norev/` — Dust yields without reverse shock destruction  
- `DustYield_rev/` — Dust yields with reverse shock destruction  

Directory Structure:
```
DustYield_norev/ or DustYield_rev/
    ├── V0/                 # Non-rotating models (v = 0 km/s)
    └── V300/               # Rotating models (v = 300 km/s)
        ├── Z1/             # [Fe/H] = 0
        ├── Z2/             # [Fe/H] = -1
        ├── Z3/             # [Fe/H] = -2
        └── Z4/             # [Fe/H] = -3
            └── data.txt
```

### Data Format (data.txt)

Each file contains:
1. Progenitor mass [Msun]
2. Total dust mass [Msun]
3. Al2O3 mass [Msun]
4. Fe mass [Msun]
5. Fe3O4 mass [Msun]
6. MgSiO3 mass [Msun]
7. Mg2SiO4 mass [Msun]
8. Amorphous carbon mass [Msun]
9. SiO2 mass [Msun]
- For `DustYield_rev`, the data additionally include ISM number density (`nISM`)

## 2. Grain Size Distributions

- `SizeDistribution_norev/` — grain size distributions with different numbers of bins without reverse shock destruction (no ISM density dependence)
- `SizeDistribution_rev/` — grain size distributions with different numbers of bins with reverse shock destruction

Directory Structure:
```
SizeDistribution_norev/ 
  ├── Nbin20/
  ├── Nbin50/
  └── Nbin100/
        ├── V0/
        └── V300/
            ├── Z1/
            ├── Z2/
            ├── Z3/
            └── Z4/
                └── M<progenitor mass>/
                    └── data.txt
```
```
SizeDistribution_rev/ 
  ├── Nbin20/
  ├── Nbin50/
  └── Nbin100/
        ├── V0/
        └── V300/
            ├── Z1/
            ├── Z2/
            ├── Z3/
            └── Z4/
                └── M<progenitor mass>/
                    ├── n1/
                    ├── n2/
                    └── n3/
                        └── data.txt
```

ISM Density Mapping
- `n1` -> 0.05 cm-3
- `n2` -> 0.5 cm-3
- `n3` -> 5 cm-3

### Data Format (data.txt)
- Column 1: Grain size [cm]
- Columns 2–8: Dust mass for each species [g]

Species are ordered as:
1. Al2O3
2. Fe
3. Fe3O4
4. MgSiO3
5. Mg2SiO4
6. Amorphous carbon
7. SiO2

## 3. Figures
*.png files show grain size distributions

Organized by stellar rotation velocity and bin number

## 4. Model Description and Citation

Details of the supernova models, dust formation, and reverse shock treatment are described in:
- K. Otaki, R. Schneider, L. Graziani, A. Bonella, S. Marassi, M. Limongi, and S. Bianchi , "Effective supernova dust yields from rotating and non-rotating stellar progenitors"
[arXiv](https://arxiv.org/abs/2506.11931v1)
[DOI](https://doi.org/10.1051/0004-6361/202555906)

## 5. Contact
- GitHub Issues
- Email: koki.otaki@uniroma1.it

Note: The affiliation will change to The University of Tokyo in April 2026.



