# HierVS: a fully AI-driven hierarchical virtual screening module.

![](https://github.com/shukai1997/HierVS/blob/main/func4.jpeg)


## Introduction

HierVS is a fully AI-driven hierarchical virtual screening module. HierVS first employs KarmaDock for efficient docking, followed by CarsiDock for accurate docking and RTMscore for re-scoring. HierVS facilitates straightforward local deployment and execution, with dynamically adjustable virtual screening duration based on the  setting of precise-docked molecular quantities.


## Installation

> Download the docker image

```
wget https://huggingface.co/gushukai/HierVS/resolve/main/hier_vs_v8.tar
```

or 

```
wget https://zenodo.org/records/15860229/files/hier_vs_v8.tar
```

> Deploy the docker image

```
docker load -i hier_vs_v8.tar
```

> Install HierVS package

```
pip install HierVS
```

## Virtual screening

You can conduct virtual screening using HierVS with:

```
HierVS -p protein_file_path -l ligand_file_path -cl compound_library_file_path -o output_path -n TopN
```

`protein_file_path` should point to the protein file (PDB); 
`ligand_file_path` should point to the reference ligand file (sdf or mol2);
`compound_library_file_path` should point to the compound library file (txt); 
`output_path` should point to the output file path;
`n` should point to the number of molecules for CarsiDock and RTMScore; 
`HierVS --help` and for more information on these input formats.


