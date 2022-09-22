# actions-run-tests
Composite GitHub action to run tests in CI/CD pipelines

## Tags

Use tag v0.1 for normal stacks. Use v0.2 for core.

### Usage

Use the tag in the github workflow for the stack in both the feature and release
yaml files:

    - name: Run tests
      uses: THIS-Institute/actions-run-tests@v0.1

### v0.1

This tag runs a command that finds tests in repos that have been set up using 
thiscovery-skeleton, i.e the location of the unit tests looks like

    .
    └── thiscovery-repo/
        ├── .github
        ├── src
        └── tests/
            ├── test_data
            └── unit_tests/
                └── test_something.py


### v0.2

This tag runs a command that finds tests in thiscovery-core, with a directory
tree that looks like

    .
    └── thiscovery-repo/
        ├── .github
        └── api/
            ├── endpoints
            └── tests/
                ├── test_data
                └── test_scripts/
                    └── unit_tests/
                        └── test_something.py
