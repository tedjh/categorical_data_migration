Categorical Data Migration
==================================

Project Description
---------------------------------
This project aims to implement the ideas introduced in Chapter 7 of
[Seven Sketches in Compositionality:An Invitation to Applied Category
Theory](https://arxiv.org/abs/1803.05316) by Spivak and Fong. In particular to model
database schemas as categories, instances of databases as functors into the category
`Set`, and to model database migrations through the use of pullbacks and adjunctions.

An implementation of this theory already exists through the
[Categorical Query Language](https://categoricaldata.github.io/) project, implemented
using Java. This project will be an exercise to replicate the same ideas and
functionality using Python instead.

Installation
-----------------------------------
First install the conda environment:
```
conda env create -f venvs/categoricaldata.yaml
```
Update the environment later using
```
conda env update -f venvs\decisiongraphormers.yaml --prune
```

Next activate the environment and install the project packages in development mode:
```
conda activate categoricaldata
pip install -e .
```
Finally, install the ``pre-commit`` git hooks using:
```
pre-commit install
```

### Testing
Unit tests should be run using pytest. This can either be done via the terminal with the command

```
pytest packages -rA
```

or by setting up a pytest configuration in pycharm.

### (Not using yet) Sphinx documentation

If compiling for the first time, create an empty directory ``.\documentation\build``. Then using PyCharm, set up a
new run configuration and choose the Sphinx option. Set the input directory to ``.\documentation\source`` and the output
directory to ``.\documentation\build``. Then run this configuration to compile the documentation.

Alternatively, from the project root directory run
```
sphinx-build documentation/source documentation/build
```
