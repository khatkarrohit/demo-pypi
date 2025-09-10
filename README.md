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
