# Singularity-Recipes

## Recipes to build Singularity Containers

### HotRec Project Containers
1./ Create a Singularity container `Base_msprime.sif` in Singularity Image Format (SIF) as root: 
Contains: `R-v3.5.3`, `snakemake-v5.10.0`, `python-v3.7.4`, `msprime-v0.7.4`, `tskit-v0.2.3`, and other packages 

`sudo singularity build Base_msprime.sif Base_msprime_Recipe-v0.1.2.def`

2./ Create a writable Singularity container `Simul_LDhelmet.sif` as root from the existing container `Base_LDhelmet.sif` in Singularity Image Format (SIF) 

`sudo singularity build --writable Simul_LDhelmet.sif LDhelmet_Singularity_Recipe.def`

### `LDhelmet_Singularity_Recipe.def` 
Recipe to build the `LDhelmet_Singularity_Recipe.sif` container


### CoGeDiv Project Containers

#### `Base.def`
Recipe to build the `Base.sif` container, which is build from `rocker/r-ver:3.5.3` and contains `python3` and `snakemake5.4.0`

#### `SuperNova2.def`
Recipe to build the `SuperNova2.sif` container, which is build from `Base.sif` and contains `supernova-2.1.1` and `longranger-2.2.2`
