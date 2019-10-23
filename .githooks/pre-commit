#!/bin/bash
#
# Called by "git commit" with no arguments.  The hook should
# exit with non-zero status after issuing an appropriate message if
# it wants to stop the commit.


find ./ -iname '*.ipynb' -not -path "./.ipynb_checkpoints/*" -print0 |
	while IFS= read -r -d '' i;
	do
		# clear all outputs in Jupyter Notebooks
		jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace "$i";
		# re-stage the cleared-out notebooks
		git add "$i";
	done;