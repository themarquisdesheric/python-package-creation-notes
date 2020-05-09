# Creating a Python Package

## Minimum Necessary Requirements 

* `README.txt` (can be empty)

* `setup.py` file

* the module itself (`vsearch.py`)

## Creating the Distribution File

1) `cd` to the module directory and run `python3 setup.py sdist`

2) if you see something like `removing 'vsearch-1.0' (and everything under it)` then it worked

This has created the `source distribution file`, in this case called `vsearch-1.0.tar.gz`. This file allows others to install the module, and can be uploaded to `PyPI` for formal use. 

## Installing the Module to `site-packages` for local use

* `cd` to the newly-created `dist` directory and run `sudo python3 -m pip install vsearch-1.0.tar.gz`

Note: we are using `sudo` to ensure we install the module with the correct permissions

`import vsearch` can now safely be used by any of our programs

## Updating the Module

Any updates to `vsearch.py` will require updating the `vsearch` module:

1) update the distribution description in `setup.py`: the `version`, `py_modules`, etc

2) generate the distribution file

3) install the module to `site-packages`
