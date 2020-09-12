# Beancount Caisse d'Epargne Importer

[![GitHub](https://img.shields.io/github/license/ArthurFDLR/beancount-ce)](https://github.com/ArthurFDLR/beancount-ce/blob/master/LICENSE)
[![PyPI](https://img.shields.io/pypi/v/beancount-ce)](https://pypi.org/project/beancount-ce/)
[![PyPI - Wheel](https://img.shields.io/pypi/v/beancount-ce)](https://pypi.org/project/beancount-ce/)
[![PyPI - Version](https://img.shields.io/pypi/pyversions/beancount-ce.svg)](https://pypi.org/project/beancount-ce/)
[![Linting](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

`beancount-ce` provides a PDF statements importer for the bank [Caisse d'Epargne](http://www.caisse-epargne.fr) to the [Beancount](http://furius.ca/beancount/) format.

## Installation

```console
    $ pip install beancount-ce
```

## Usage

```python
    IBAN_NUMBER_CE = 'FR00 1111 2222 3333 4444 5555 666'

    CONFIG = [
        CEImporter(
            iban=IBAN_NUMBER_CE,
            account='Assets:FR:CdE:CompteCourant',
            expenseCat='Expenses:FIXME',    #Optional
            creditCat='Income:FIXME',       #Optional
            showOperationTypes=False        #Optional
        ),
    ]
```

## Contribution

Feel free to contribute!

Please make sure you have Python 3.6+ and [`Poetry`](https://poetry.eustace.io/) installed.

1. Git clone the repository - `git clone https://github.com/siddhantgoel/beancount-n26`

2. Install the packages required for development - `poetry install`

3. That's basically it. You should now be able to run lint checks and the test suite - `make lint test`.
