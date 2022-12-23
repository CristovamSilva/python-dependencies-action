## Python-Dependencies-Action

This action provides the following functionality for GitHub Actions users:

-   Checks-out your repository under $GITHUB_WORKSPACE, so your workflow can access it. 

-   Install a version of Python.

-   Cache dependencies for Pip.

-   (Optional) Install your application modules as described in **requirements.txt**.

-   (Optional) Install Quality Assurance dependencies such as **isort, black, mypy flake8, and pylint** and any other present in **requirements-qa.txt**.

-   (Optional) Install Security Assurance dependencies such as **bandit** and any other present in **requirements-sec.txt**.

-   (Optional) Install Test dependencies such as **pytest** and **pytest-cov** and any other present in **requirements-test.txt**.

### Basic Usage

```yaml
-   name: Setup Cache & Dependencies
    uses: cristovamsilva/python-dependencies-action@master
    with:
        python-version: '3.9'           # Default is 3.10
        deps-directory: ./requirements  # Where to search for the requirements*.txt files.
        application: true               # Whether to install application modules.
        quality: true                   # Whether to install qa dependencies.
        security: true                  # Whether to install security dependencies.
        test: true                      # Whether to install test dependencies.
```
