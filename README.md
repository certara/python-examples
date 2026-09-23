# Chemaxon Python API examples

This repository contains usage examples for [Chemaxon Python API](https://docs.chemaxon.com/display/docs/python-api_index.md).
For each notebook (ipynb) file the corresponding py file contain the pure python commands. This python file has a clear git history without generated cell outputs.

## Prerequisites

- Chemaxon license key (or license file). See the [documentation](https://docs.chemaxon.com/display/docs/python-api_installation.md#license-installation) for details.
- [JupyterLab](https://jupyter.org/install) for Jupyter notebook examples.

## Continuous Integration

A [workflow](.github/workflows/example-notebooks.yml) executes every numbered example notebook
against the newest `chemaxon` release on each push/PR to `main`. It only checks that the code
runs without error - outputs are not validated. This is meant to catch API changes that break an
example without the example being updated in the same commit.

The workflow needs two repository secrets:

- `CHEMAXON_PYPI_INDEX_URL` - the authenticated index URL for Chemaxon's private package index
  (the same URL used in your local pip config to install `chemaxon`).
- `CHEMAXON_LICENSE_SERVER_KEY` - a license key valid for the Python API.

## Note

If you have any question, suggestion please feel free to contact us via
[Chemaxon Support Portal](https://chemaxon.freshdesk.com/a/tickets/new)

## Contributors 

- For contributors only: install [jupytext](https://jupytext.org/), which will enable synchronization of notebook and python (ipynb and py) files.
- If pairing newly created notebook and python files is needed: `ls jupyter/*.ipynb | xargs jupytext --set-formats ipynb,py:percent` will generate the python file and pair the notebook file with it.
