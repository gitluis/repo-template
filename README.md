# Repository Name

Repository description.

* [Repository](#repository)
   * [Branches](#branches)
   * [File Structure](#file-structure)
* [Software Best Practices](#software-best-practices)
   * [Development](#development)
   * [Documentation](#documentation)
* [Contribution](#contribution)
    * [Branch Naming Convention](#branch-naming-convention)
    * [How-to Contribute](#how-to-contribute)
    * [Pull Requests](#pull-requests)


# Repository


## Branches

| Branch   | Description                        | Reviews Required | Comments                                |
|:---------|:-----------------------------------|:----------------:|:----------------------------------------|
| `master` | Official software release          | 1                |                                         |
| `qa`     | Quality assurance software release | 2                | Software reviews, team discussion, etc. |
| `dev-*`  | All software development branches  | 0                | `*` represents the branch name          |

See [Branch Naming Convention](#branch-naming-convention) for guidelines on naming development branches.


## File Structure

| Item         | Description                                                  |
|:-------------|:-------------------------------------------------------------|
| `docs/`      | API Reference documentation                                  |
| `notebooks/` | Python notebooks                                             |
| `output/`    | Software output code & tests                                 |
| `src/`       | Software source code                                         |
| `tests/`     | Unit tests for each function or method within AI pkg modules |
| `.gitignore` | List of files or dirs to exclude in the repository           |
| `README.md`  | This document                                                |


# Software Best Practices

The following is a collection of software best practices we follow or have adopted and used in our toolbox software code along with some exceptions.


## Development

In regards to software development, we use the following guidelines:
* [The Zen of Python](https://www.python.org/dev/peps/pep-0020/#id2)
* [Pandas code style guide](https://pandas.pydata.org/pandas-docs/stable/development/code_style.html)
* [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)


### Exceptions

Python Language Rules:
| Rule                  | Recommendation                            |
|:----------------------|:------------------------------------------|
| `global` variables    | Avoid using global variables              |
| `list` comprehensions | Okay to use for simple and readable cases |
| `set` comprehensions  | Okay to use for simple and readable cases |
| `dict` comprehensions | Okay to use for simple and readable cases |

Python Style Rules:
| Rule                 | Recommendation |
|:---------------------|:---------------|
| Line length          | 120 characters |
| Indentation          | 4 spaces |
| Naming conventions   | Follow [Google's naming convention](https://google.github.io/styleguide/pyguide.html?showone=Naming#316-naming) rules for naming classes, methods, functions, variables, etc. |
| Functions / methods  | End all functions and methods with a `return` statement including the `__init__` constructor method |
| Parentheses          | Use in math operations, strings and logical operations only |
| Comments             | Use multiple pound `#` symbols for block or in-line comments |
| Docstrings           | Use three double quotes `"""` for all docstrings |


## Documentation


### Docstrings

All class, methods and function docstrings are built following the [pandas docstring guide](https://pandas.pydata.org/pandas-docs/stable/development/contributing_docstring.html).


### API Reference

The `docs/` folder holds all web-based software development documentation that is auto-generated using [Sphinx](http://www.sphinx-doc.org/en/stable/index.html).

Examples:
* [Pandas DataFrame class example](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html)

Resources:
* [Sphinx Getting Started](http://www.sphinx-doc.org/en/stable/usage/quickstart.html)
* [Sphinx Simple Tutorial](https://brandons-sphinx-tutorial.readthedocs.io/en/latest/)
* [An idiot’s guide to Python documentation with Sphinx and ReadTheDocs](https://samnicholls.net/2016/06/15/how-to-sphinx-readthedocs/)


# Contribution

For those team members willing to contribute to the toolbox make sure you understand the content hereby explained before doing anything.


## Branch Naming Convention

All development branches are to be named after `dev-*` where `*` shall be replaced by the branch name. The branch name shall reflect what the branch was created for or intended to be worked on (defect/bug fix, addition, enhancement, etc.).

Examples:
| Branch Purpose                        | Bad Name         | Good Name                |
|:--------------------------------------|:-----------------|:-------------------------|
| Create a new LASSO module             | `dev-add-module` | `dev-add-lasso-module`   |
| Fix bug in P-values module's function | `dev-fix-bug`    | `dev-fix-pvalues-bug`    |
| Refactor Logistic Regression module   | `dev-change-lr`  | `dev-refactor-lr-module` |

Remember, **explicit is better than implicit** (add, fix, refactor, bug/defect, improve/enhance).


## How-to Contribute

1. Create a local branch
2. Create/modify unit test cases
3. Add/commit software changes
4. Run unit test cases
    * Back to step 2 upon failures
5. Push local branch to remote repository
    * `git push origin dev-*`
6. Create a pull-request against `qa` branch
7. Request feedback from peers or reviewers

## Pull Requests

1. Implement changes requested
   * As agreed on per team discussions
2. Run unit test cases
   * Back to step 1 upon failures
3. Push new changes implemented
4. Repeat steps 1-3 until team agreement
5. Run unit test suite from `qa` branch
   * All tests must pass
6. If test suite passes, approve review changes
   * Back to step 1 upon failures
7. Merge changes in `qa` to `master` branch
