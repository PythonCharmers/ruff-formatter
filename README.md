# Ruff-formatter Extension For Quarto

A [Quarto](https://quarto.org/) filter to format the Python code using [ruff](https://docs.astral.sh/ruff/formatter/)


## Installing

```bash
quarto add PythonCharmers/ruff-formatter
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

Make sure `ruff` is installed. See [here](https://docs.astral.sh/ruff/installation/) for installation instructions.


## Using

Add the filter in your Quarto document like this:

```
---
filters:
  - ruff-formatter
---
```

It is possible to configure `ruff` via a `pyproject.toml` or `ruff.toml` file: see [here](https://docs.astral.sh/ruff/configuration/).

For example, suppose you want to use 80 characters per line i.e. `--line-length=80`. (Ruff defaults to 88 character per line.) You can specify the following in the `pyproject.toml` file under `[tool.ruff]`,

```
[tool.ruff]
line-length = 80
```

And then place this toml file in the same directory as the qmd file of the Python code chunks you want to format.


## Credits

Thanks to Shafayet Shafee for his [Black formatter for Quarto](https://github.com/shafayetShafee/black-formatter) for inspiration!
