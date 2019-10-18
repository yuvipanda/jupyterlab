# @jupyterlab/debugger

[![Build Status](https://dev.azure.com/jupyterlab/jupyterlab/_apis/build/status/jupyterlab.debugger?branchName=master)](https://dev.azure.com/jupyterlab/jupyterlab/_build/latest?definitionId=3&branchName=master)

A JupyterLab debugger UI extension

This extension is under active development and is not yet available.

## Prerequisites

- JupyterLab 1.1+
- xeus-python 0.5+

## Development

```bash
# Create a new conda environment
conda create -n jupyterlab-debugger -c conda-forge jupyterlab nodejs xeus-python=0.5.3 ptvsd

# Activate the conda environment
conda activate jupyterlab-debugger

# Install dependencies
jlpm

# Build Typescript source
jlpm build

# Link your development version of the extension with JupyterLab
jupyter labextension link .

# Rebuild Typescript source after making changes
jlpm build

# Rebuild JupyterLab after making any changes
jupyter lab build

# Start JupyterLab with the kernel logs enabled and watch move enabled
XEUS_LOG=1 jupyter lab --no-browser --watch
```

### Tests

To run the tests:

```bash
# [Optional] to enable the logs for xeus-python
export XEUS_LOG=1

jlpm run test
```

### Inspecting debug messages

The [kernelspy extension for JupyterLab](https://github.com/vidartf/jupyterlab-kernelspy) can be used to inspect the debug messages sent between the debugger UI and the kernel.

To install it:

```bash
jupyter labextension install jupyterlab-kernelspy
```
