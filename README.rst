Bit: Bitcoin made easy.
=======================

.. image:: https://img.shields.io/pypi/v/bit.svg?style=flat-square
    :target: https://pypi.org/project/bit

.. image:: https://img.shields.io/travis/ofek/bit.svg?branch=master&style=flat-square
    :target: https://travis-ci.org/ofek/bit

.. image:: https://img.shields.io/codecov/c/github/ofek/bit.svg?style=flat-square
    :target: https://codecov.io/gh/ofek/bit

.. image:: https://img.shields.io/pypi/pyversions/bit.svg?style=flat-square
    :target: https://pypi.org/project/bit

.. image:: https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square
    :target: https://en.wikipedia.org/wiki/MIT_License

-----

Bit is Python's fastest Bitcoin library and was designed from the beginning to
feel intuitive, be effortless to use, and have readable source code. It is
heavily ispired by `Requests <https://github.com/kennethreitz/requests>`_ and
`Keras <https://github.com/fchollet/keras>`_.

**Bit is so easy to use, in fact, you can do this:**

.. code-block:: python

    >>> from bit import Key
    >>>
    >>> my_key = Key(...)
    >>> my_key.get_balance('usd')
    '12.51'
    >>>
    >>> # Let's donate!
    >>> outputs = [
    >>>     # Wikileaks
    >>>     ('1HB5XMLmzFVj8ALj6mfBsbifRoD4miY36v', 0.0035, 'btc'),
    >>>     # Internet Archive
    >>>     ('1Archive1n2C579dMsAu3iC6tWzuQJz8dN', 190, 'jpy'),
    >>>     # The Pirate Bay
    >>>     ('129TQVAroeehD9fZpzK51NdZGQT4TqifbG', 3, 'eur'),
    >>>     # xkcd
    >>>     ('14Tr4HaKkKuC1Lmpr2YMAuYVZRWqAdRTcr', 2.5, 'cad')
    >>> ]
    >>>
    >>> my_key.send(outputs)
    '9f59f5c6757ec46fdc7440acbeb3920e614c8d1d247ac174eb6781b832710c1c'

Here is the transaction `<https://blockchain.info/tx/9f59f5c6757ec46fdc7440acbeb3920e614c8d1d247ac174eb6781b832710c1c>`_.

Features
--------

- Seamless integration with existing server setups
- Fully supports 25 different currencies
- First class support for storing data in the blockchain
- Access to the blockchain (and testnet chain) through multiple APIs for redundancy
- Exchange rate API, with optional caching
- Optimal transaction fee API, with optional caching
- Compressed public keys by default
- Multiple representations of private keys; WIF, PEM, DER, etc.
- Standard P2PKH transactions

If you are intrigued, continue reading. If not, continue all the same!

Installation
------------

Bit is distributed on `PyPI`_ as a universal wheel and is available on Linux/macOS
and Windows and supports Python 3.3+ and PyPy3.3-5.5+.

.. code-block:: bash

    $ pip install bit

Documentation
-------------

Docs are `hosted by Github Pages`_ and are automatically built and published
by Travis after every successful commit to Bit's ``master`` branch.

Credits
-------

- Logo courtesy of `<https://textcraft.net>`_
- `Gregory Maxwell`_ (Bitcoin core dev) for teaching me a bit of `ECC`_ math
- `arubi`_ in #bitcoin for helping me understand transaction gotchas
- `fuzeman`_ for bestowing me the name `bit` on the `Python Package Index`_

.. _PyPI: https://pypi.org/project/bit
.. _hosted by Github Pages: https://ofek.github.io/bit
.. _Gregory Maxwell: https://github.com/gmaxwell
.. _ECC: https://en.wikipedia.org/wiki/Elliptic_curve_cryptography
.. _arubi: https://github.com/fivepiece
.. _fuzeman: https://github.com/fuzeman
.. _Python Package Index: https://pypi.org
