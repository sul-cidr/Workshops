[![Center for Interdisciplinary Digital Research @ Stanford](https://raw.githubusercontent.com/sul-cidr/Workshops/master/cidr-logo.no-text.240x140.png)](https://cidr.stanford.edu)

# Workshops
Code and documentation for CIDR workshops

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sul-cidr/Workshops/blob/master/Data_Manipulation_with_Python/Data%20Manipulation%20with%20Python.ipynb) Data Manipulation with Python


## Development
If you're developing Jupyter Notebooks in this repo, note that there is a git `pre-commit` hook which is used to clear all cell output before notebooks are committed.  To activate the hook, ensure it is executable (`chmod +x .githooks/*`) and set the `core.hooksPath` config variable in your local clone of the repo (`git config core.hooksPath .githooks`).
