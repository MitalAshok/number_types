number\_types
=============

Various number types for Python

Usage
-----

`Typed complex <https://github.com/MitalAshok/number_types/blob/master/number_types/typed_complex.py>`__
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use a complex number with different types for its real and imaginary
parts:

.. code:: python

    >>> from number_types.typed_complex import *
    >>> z = DecimalComplex('0.2', '0.1')
    >>> z + DecimalComplex('0.1', '0.2')
    DecimalComplex(Decimal('0.3'), Decimal('0.3'))
    >>> z = complex(0.2, 0.1)
    >>> z + complex(0.1, 0.2)
    (0.30000000000000004+0.30000000000000004j)

`Coordinates <https://github.com/MitalAshok/number_types/blob/master/number_types/coordinates.py>`__
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A class representing a (2D) coordinate.

.. code:: python

    >>> from number_types import Coordinate
    >>> Coordinate(0, 1) + Coordinate(1, 0)
    >>> Coordinate(1, 1)
    >>> Coordinate(-1, 0).to_polar()
    Coordinate(1.0, 3.141592653589793, False)
    >>> Coordinate(-1, 0).to_polar().equals(Coordinate(-1, 0))
    True
    >>> Coordinate(3, 4).to_polar()
    Coordinate(5.0, 0.9272952180016122, False)
    >>> abs(Coordinate(3, 4))
    5.0
    >>> Coordinate(3, 4).conjugate
    Coordinate(3, -4)

Installing
----------

From `PyPI <https://pypi.org/project/number_types/>`__
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

    $ pip install number_types

From source
~~~~~~~~~~~

.. code:: bash

    $ git clone 'https://github.com/MitalAshok/number_types.git'
    $ python ./number_types/setup.py install
