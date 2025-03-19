# Pre-built Pyodide wheels for CLiC

A set of pyodide wheels for using FlexiConc under CLiC.

## Rebuilding locally

Firstly, ensure your local build environment is set up:

    apt install build-essential autoconf automake libtool

Also, python 3.12 is required. Compile if necessary:

    https://docs.brucerenner.com.au/posts/Debian-Buster-Python-Install/

Then, run ``./build.sh``. In ~20mins, you should have rebuilt wheels in this directory.

## LibICU locales

The ``./build.sh`` script defines a ``ICU_DATA_FILTER_FILE`` to include a minimal number of locales.
Modify the ``filters.json`` definition to include more locales in the icudata wheel.

## Rebuilding under GitHub

You can [manually trigger the GitHub action](https://docs.github.com/en/actions/managing-workflow-runs-and-deployments/managing-workflow-runs/manually-running-a-workflow),
which will build & commit a new version of all wheels.

