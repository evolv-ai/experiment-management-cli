Evolv CLI
====================================

[![image](https://img.shields.io/pypi/v/evolvcli.svg)](https://pypi.org/project/evolvcli/)
[![image](https://img.shields.io/pypi/l/evolvcli.svg)](https://pypi.org/project/evolvcli/)
[![image](https://img.shields.io/pypi/pyversions/evolvcli.svg)](https://pypi.org/project/evolvcli/)

The experiment management CLI provides functionality to create and maintain Evolv experiments.

## Setup

Pre-requisites: You must have Python 3.7 installed on your computer.

1. Create a Python virtual environment and install the cli.
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    pip install evolvcli
    ```
    
2. Ensure the CLI is properly installed by calling the cli. You must be in the virtual environment
   you created to use the cli. 
    ```bash
    evolv
    ```
    You should see a help menu appear in your terminal.

## Quickstart

To start using the CLI obtain your account id from Evolv staff.

1. Export your account id as an environment variable.

    ```bash
    export EVOLV_ACCOUNT_ID=<your account id>
    ```
    
2. To test the cli is working use the "get account" command.

    ```bash
    evolv get account
    ```
    
3. The system will prompt you to enter your Evolv email and password.

4. Once logged in you will not have to login again till your credentials expire.

## Other Commands

To find out more about the CLI commands and how to use them use the `--help` option.

For example: `evolv get --help`

Possible sub commands include:

```bash
evolv get
evolv list
evolv create
evolv update
```

## Developing

When developing theres some key things to know. 

### Setup

1. Create a Python virtual environment and install the cli.
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    pip install -r requirements-dev.txt
    python setup.py develop
    ```
    
2. Ensure the CLI is properly installed by calling the cli. You must be in the virtual environment
   you created to use the cli. 
    ```bash
    evolv
    ```
    You should see a help menu appear in your terminal.
    
### Uploading to PyPi

Make sure you are at the project root for these steps.

1. Update the version of the package found in: [./setup.py] (Make sure to check this in.)

2. Enter your virtual environment and upload the package.
    ```bash
    source .venv/bin/activate
    python setup.py sdist
    twine upload dist/evolvcli-<version>.tar.gz
    ```
 
3. Twine will prompt you for credentials, get these from the Evolv Engineering Team.