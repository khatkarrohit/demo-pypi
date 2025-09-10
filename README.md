# A Demonstration Package

This is a simple demonstration package. You can use it to learn how to publish your own packages on PyPI.

## Usage

To use this library in your own project, you can import the `add_one` function like this:

```python
from demo_pypi import add_one

result = add_one(5)
print(result)  # Output: 6
```

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

## Troubleshooting

**Error: `ModuleNotFoundError: No module named 'demo_pypi'`**

If you have installed the package locally but are still getting a `ModuleNotFoundError`, here are some things to check:

1.  **Correct Python Environment**: Make sure you are using the same Python interpreter or virtual environment where you installed the package. You can check the path to your Python executable by running `which python` (on macOS/Linux) or `where python` (on Windows).

2.  **Check Installed Packages**: Verify that the package is listed when you run `pip list`.

3.  **IDE/Editor Configuration**: Sometimes, your IDE or editor might be using a different Python interpreter than the one in your terminal. Check your IDE's settings to ensure it's pointing to the correct Python environment.

4.  **Restart Your IDE/Terminal**: After installing a new package, it's sometimes necessary to restart your IDE or terminal session for the changes to take effect.
