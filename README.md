# Manage ocean4dVarnet Contributions

- [Tools](./scripts/README.md)
- [Contributions](./contrib/README.md)

[![Validate Contributions](https://github.com/ebraux/ocean4dvarnet-contrib/actions/workflows/validate_contrib.yml/badge.svg)](https://github.com/ebraux/ocean4dvarnet-contrib/actions/workflows/validate_contrib.yml)

# Organization Summary

1. Contribution structure: Each contribution resides in a dedicated folder with a `metadatas.yml` file containing required information (date, description, contact, etc.).
2. Automatic validation: A Python script integrated into CI (GitHub Actions, GitLab CI, etc.) validates the presence of required fields.
3. Documentation generation: A script extracts these details and renders them into a markdown file or directly into the project documentation.
4. CI pipeline: Validation and documentation generation are automated in your CI pipeline.
