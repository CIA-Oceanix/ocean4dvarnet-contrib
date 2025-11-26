# Creating a New Contribution

A contribution must contain at least:

```bash
contrib/
├── <CONTRIB_NAME>
│   ├── __init__.py
│   ├── metadatas.yml
│   ├── README.md
│   ├── <CONTRIB_NAME>.py
│   └── tests/
│       └── test_<CONTRIB_NAME>.py
```

- `__init__.py`: module configuration file, can be empty
- `metadatas.yml`: information about the contribution (author, description, ...)
- `README.md`
- `<CONTRIB_NAME>.py`: your code
- `tests`: optional test files

It may also include:

- `requirements.txt`
- `pyproject.toml`
- `LICENSE.md`
- other Python source files

To initialize a new contribution, use the script `init-new-contrib`:
```bash
python3 scripts/init_contrib.py <YOUR_CONTRIB_NAME>
```

The contribution name must only contain lowercase letters, digits, and underscores.

If the name is valid, a folder will be created in `contrib` with the files `README.md` and `metadatas.yml`, initialized with default values.

For example:
```bash
python3 scripts/init_contrib.py example_contrib
```
The script will create:

- `contrib/example_contrib/README.md` with:
```bash
# example_contrib
```

- `contrib/example_contrib/metadatas.yml` with:
```yaml
name: "example_contrib"
description: "example_contrib"
date: "2025-04-01"
contact: "contributor1@example.com"
version: "1.0.0"
license: "CeCILL-C FREE SOFTWARE LICENSE AGREEMENT"
dependencies: ""
```


For inclusion in the repository, the contribution will be evaluated with code quality tools (`pylint`, ...).

Tests are not mandatory but strongly recommended. The code is tested with `pytest`.
