# A Demonstration Package

This is a simple demonstration package. You can use it to learn how to publish your own packages on PyPI.

## Documentation

For more detailed documentation, please see [DOCS.md](DOCS.md).

## Building and Publishing

To build and publish this package, follow these steps:

1. **Install the build tools**:

   ```bash
   pip install build twine
   ```

2. **Build the package**:

   ```bash
   python -m build
   ```

3. **Check the package**:

   ```bash
   twine check dist/*
   ```

4. **Upload to TestPyPI**:

   ```bash
   twine upload --repository testpypi dist/*
   ```

5. **Upload to PyPI**:

   ```bash
   twine upload dist/*
   ```

## Local Installation

To install this library locally for use in other projects, you can use one of the following methods:

### 1. Install from a local source directory

This method is useful when you want to test the package in another local project without publishing it. Navigate to the root directory of this project and run:

```bash
pip install .
```

### 2. Install in editable mode

This method is useful when you are actively developing the package and want the changes to be reflected immediately in the other projects that use it. Navigate to the root directory of this project and run:

```bash
pip install -e .
```
