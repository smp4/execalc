# execalc

> execalc replaces Microsoft Excel with Python and [Jupyter Book](https://jupyterbook.org) to create, document and share testable, repeatable and accessible technical calculations.

-----

**Table of Contents**

- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Thanks](#thanks)
- [To Do](#todo)

The demo book from this repository is available [here](https://smp4.github.io/execalc/).

## Installation

Calculation templates are generated with [`cruft`](https://cruft.github.io/cruft/).

Install `cruft`.

```bash
pip3 install cruft
```

Generate a calculation template.

```bash
cruft create https://github.com/smp4/......::::
```

Answer the questions to auto-fill the template parameters.


## Usage

The calculation exists in the Python source code in the `src` directory.

The calculation document is a Jupyter Book, stored in the `book` directory. It references the Python code in `src?`.

The target audience of the calculation document in the `book` directory is anyone that needs to verify, validate, consume or review the calculation. There are some audiences that may need to interact with your calculation, but might want to do things outside of the scope of a technical document. For example, sysadmins, other engineers/ developers etc may be interested in infrastructure, deployment, development of the source Python code. Documentation relevant to these users is stored in the `docs` folder. This folder contains documentation traditionally aligned with a normal software project.

After editing the book:

```console
hatch run book:jbbuild  # build the book
hatch run book:jbpublish  # publish to gh-pages
git add .
git commit -m "message"
git push
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## License

todo..


## Thanks

This `README.md` was inspired by [Make a README](https://www.makeareadme.com/).


## To Do

* get prototype working
* cruft template# License
* check licenses of all used tools and libraries, that is ok to use them commercially. pick a license for this repo that fits.
* references/ citations
* where and how to set up jupyter kernel to build the book. does it use the default env of the project? shall the default env by the computational env of the calc?
