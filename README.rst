# GPCRchimeraDB documentation - ReadTheDocs

This repository contains the documentation for "GPCRchimeraDB". The documentation is generated using Sphinx and hosted on Read the Docs.

## Getting Started

### Prerequisites

Make sure you have Python and pip installed. You can check your installations by running:

```bash
python --version
pip --version
```

### Prerequisites

Make sure you have Anaconda or Miniconda installed. You can download and install it from [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

### Installation

1. Clone the repository:
```bash
git clone git@github.com:Bio2Byte/gpcrchimeradb-docs.git
cd gpcrchimeradb-docs
```

2. Create a new conda environment with Python 3:
```bash
conda create --name gpcrchimeradb-docs python=3
conda activate gpcrchimeradb-docs
```

3. Install the required packages:
```bash
cd docs
pip install -r requirements.txt
```


### Building the Documentation

1. Build the HTML documentation using the make command:
```bash
make html
```
2. Add, commit and push the changes. A minute later the changes are visible on the webserver!