Evolv Experiment SDK for Python
=====================

This will serve as the resting place of the Python Evolv Experiment SDK.

Supported Python Versions
-------------------------

The Evolv SDK is only compatible with Python 3.7 or above.

Installing
----------

1. Create a virtualenv for the project.

        $ python3 -m venv .venv
        $ source .venv/bin/activate
        
2. Install it's dependencies.

        $ pip install -r requirements.txt
        
Testing and Coverage
--------------------

To run unit tests and see test coverage:

        $ coverage run -m unittest discover
        $ coverage report -m
        
Linting
-------

To run the flake8 linter:

        $ flake8 .