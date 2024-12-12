
# Guidelines to update the documentation

## Getting Started

### Prerequisites

1. **Python and pip**: Ensure Python and pip are installed. Verify your installation by running:

    ```bash
    python --version
    pip --version
    ```

2. **Conda**: Install Anaconda or Miniconda. Download from [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

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

2. Add, commit, and push the changes. After about a minute, the updates will be visible on the web server!
