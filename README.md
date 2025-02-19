# python_pkg_template

***NOTE:*** This repository is different from the original template in only one way, which is that all packages live under `src/rpad` instead of `src` - this allows us to put all of the shared r-pad code in one namespace so that you can import from `rpad.<package>` in Python. This is nice because it makes it clear which code is lab-specific and which isn't.

This is a template for a python package with the following features:

* Installable via `pip install`. Anyone can point directly to this Github repository and install your project, either as a regular dependency or as an editable one.
* Uses the new [PEP 518, officially-recommended pyproject.toml](https://pip.pypa.io/en/stable/reference/build-system/pyproject-toml/) structure for defining project structure and dependencies (instead of requirements.txt)
* Nice, static documentation website support, using mkdocs-material. Structure can be found in `docs/`
* `black` support by default, which is an opinionated code formatting tool
* `pytest` support, which will automatically run tests found in the `tests/` directory
* `mypy` support, for optional typechecking of type hints
* `pre-commit` support, which runs various formatting modifiers on commit to clean up your dirty dirty code automatically.
* Github Actions support, which runs the following:
    * On a Pull Request: install dependencies, run style checks, run Python tests
    * After merge: same a Pull Request, but also deploy the docs site to the projects Github Pages URL!!!!

All that needs doing is replacing all occurances of `python_pkg_template` and `python-pkg-template` with the name of your package(including the folder `src/rpad/python_pkg_template`), the rest should work out of the box!
