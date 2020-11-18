[![Center for Interdisciplinary Digital Research @ Stanford](https://raw.githubusercontent.com/sul-cidr/Workshops/master/cidr-logo.no-text.240x140.png)](https://cidr.stanford.edu)

# Workshops
Code and documentation for CIDR workshops

For a list of CIDR's current offerings, visit [cidr.stanford.edu/workshops](https://cidr.stanford.edu/workshops).  A full program of workshops offered by Stanford University Libraries, including CIDR workshops and others, can be found at [library.stanford.edu/workshops](https://library.stanford.edu/workshops).

## Development
If you're developing Jupyter Notebooks in this repo, the recommended approach is to develop using a local Jupyter server.  Although editing a notebook in Colaboratory and saving it back to the repo is possible, it can make the commit history a bit messy and is not ideal.  If you are developing locally, note that there is a git `pre-commit` hook which is used to clear all cell output before notebooks are committed.  To activate the hook, ensure it is executable (`chmod +x .githooks/*`) and set the `core.hooksPath` config variable in your local clone of the repo (`git config core.hooksPath .githooks`).
