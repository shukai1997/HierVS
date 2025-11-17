# HierVS: a fully AI-driven hierarchical virtual screening module.

![](https://github.com/shukai1997/HierVS/blob/main/func4.jpeg)


## Introduction

HierVS is a fully AI-driven hierarchical virtual screening module. HierVS first employs KarmaDock for efficient docking, followed by CarsiDock for accurate docking and RTMscore for re-scoring. HierVS facilitates straightforward local deployment and execution, with dynamically adjustable virtual screening duration based on the  setting of precise-docked molecular quantities.

## System Requirements

| Component | Specification |
|-----------|---------------|
| **Operating System** | Ubuntu 22.04.5 |
| **Processor** | Intel(R) Core(TM) i9-14900KF |
| **GPU** | NVIDIA GeForce RTX 4090 |
| **Storage** | Minimum 24 GB of available hard-disk space |
| **CUDA** | Version 12.4 |
| **NVIDIA GPU Driver** | Version 550.144.03 |
| **Docker** | Version 28.0.1 |
| **Package Management** | PyPI (Python package management tool) |

*The software and hardware listed above are recommended, as our testing was conducted in this environment. Other software or hardware configurations may also be capable of running this tool properly.*

## Installation

### 📥 Step 1: Download Docker Image
*(Download time depends on your network speed)*

Choose one of the following download sources:

**Option A - Hugging Face:**
```
wget https://huggingface.co/gushukai/HierVS/resolve/main/hier_vs_v9.tar.gz
```
**Option B - Zenodo:**
```
wget https://zenodo.org/records/15860229/files/hier_vs_v8.tar
```


### 📥 Step 2: Deploy the docker image
*(Takes several seconds to minutes)*
```
docker load -i hier_vs_v8.tar
```

### 📥 Step 3: Install HierVS package
*(Takes several seconds )*
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


