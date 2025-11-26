# generate_contrib_docs

---

::: scripts.generate_contrib_docs

The function read_pyproject_metadata returns only the [project] section.

Authors are properly formatted if provided as a list.

This code uses tomllib, available natively from Python 3.11; for Python 3.10 or lower it uses tomli.

- Dynamically detects the Python version
- Uses tomllib if available (Python 3.11+), otherwise falls back to tomli
- Includes a clear error message if tomli is not installed on Python < 3.11
