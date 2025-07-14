# HierVS: a fully AI-driven hierarchical virtual screening module.

![](https://github.com/shukai1997/HierVS/blob/main/func4.jpeg)


## Introduction

HierVS is a fully AI-driven hierarchical virtual screening module. HierVS first employs KarmaDock for efficient docking, followed by CarsiDock for accurate docking and RTMscore for re-scoring. HierVS facilitates straightforward local deployment and execution, with dynamically adjustable virtual screening duration based on the  setting of precise-docked molecular quantities.


## Installation

> Note: we recommend installing boltz in a fresh python environment

Install boltz with PyPI (recommended):

```
pip install boltz -U
```

or directly from GitHub for daily updates:

```
git clone https://github.com/jwohlwend/boltz.git
cd boltz; pip install -e .
```

## Inference

You can run inference using Boltz with:

```
boltz predict input_path --use_msa_server
```

`input_path` should point to a YAML file, or a directory of YAML files for batched processing, describing the biomolecules you want to model and the properties you want to predict (e.g. affinity). To see all available options: `boltz predict --help` and for more information on these input formats, see our [prediction instructions](docs/prediction.md). By default, the `boltz` command will run the latest version of the model.


