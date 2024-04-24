# A deep dive into the Arrow Columnar format with pyarrow and nanoarrow

Repository for the Arrow Columnar Format Tutorial at PyCon DE & PyData Berlin 2024.

Apache Arrow has become a de-facto standard for efficient in-memory columnar data representation. You might have heard about Arrow or using Arrow, but do you understand the format and why it's so useful? This tutorial will dive deep into the details of the Arrow columnar format, the different types and buffer layouts, and explore those details interactively using the pyarrow and nanoarrow libraries.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/voltrondata-labs/2024-arrow-format-tutorial/HEAD?labpath=intro.ipynb)

## Setup

To run this tutorial locally, follow those steps:

**Clone this repository**

    git clone https://github.com/voltrondata-labs/2024-arrow-format-tutorial.git

**Install the necessary packages**

The code examples require numpy, pyarrow and [nanoarrow](https://github.com/apache/arrow-nanoarrow), and JupyterLab (or alternative) to run the notebooks. We need the latest (not-yet-released) version of nanoarrow, but you can install that using the nightly wheels:

    pip install jupyterlab numpy pandas pyarrow
    pip install --extra-index-url https://pypi.fury.io/arrow-nightlies/ --pre nanoarrow

We recommend to create an environment, either with conda/mamba:

    conda create -n arrow-tutorial python numpy pandas jupyterlab
    conda activate arrow-tutorial
    python -m pip install pyarrow
    python -m pip install --extra-index-url https://pypi.fury.io/arrow-nightlies/ --pre nanoarrow

or create a virtual environment:

    cd 2024-arrow-format-tutorial
    python -m venv .venv
    source .venv/bin/activate
    pip install jupyterlab numpy pandas pyarrow
    pip install --extra-index-url https://pypi.fury.io/arrow-nightlies/ --pre nanoarrow

**Launch Jupyter**

From the repo directory:

    jupyter lab
