# Workshops
Code and documentation for CIDR workshops


## Development
If you're developing Jupyter Notebooks in this repo, note that there is a git `pre-commit` hook which is used to clear all cell output before notebooks are committed.  To activate the hook, ensure it is executable (`chmod +x .githooks/*`) and set the `core.hooksPath` config variable in your local clone of the repo (`git config core.hooksPath .githooks`).
