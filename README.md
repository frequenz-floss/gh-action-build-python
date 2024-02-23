# Build Python Action

This action builds Python wheels and source distribution for a Python package.

Here is an example demonstrating how to use it in a workflow:

```yaml
jobs:
  build:
    name: Build
    runs-on: ubuntu-20.04

    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      - name: Build wheels
        uses: frequenz-floss/gh-action-build-python@v0.x.x
        with:
          python_version: "3.11"
```

## Inputs

* `python_version`: The Python version to use. Required.

   This is passed to the `actions/setup-python` action.

* `outdir`: The directory where the built packages will be placed.
