# Software Best Practices

The following is a collection of software best practices we follow or have adopted and used in our toolbox software code along with some exceptions.

* [Software Best Practices](#software-best-practices)
   * [Development](#development)
   * [Documentation](#documentation)


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