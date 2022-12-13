Python List Comprehensions
==========================

--------------

List Comprehensions
===================

* Used to create lists using ``for`` and ``if`` clauses
* Introduced in Python 2.0
* This feature was introduced via PEP202


--------------

For loop
========

* Traditional imperative programming method, use a ``for`` loop

Create a list of the first ten powers of two:

.. sourcecode:: python

    powersof2 = []
    for x in range(1, 11):
        powersof2.append(2 ** x)

    >>> print powersof2
    [2, 4, 8, 16, 32, 64, 128, 256, 512, 1024]

--------------

Map function
============

* Functional programming approach
* Apply function to each item returned by iterable
* Syntax: ``map(function, iterable)``

Powers of two example with ``map`` and anonymous ``lambda`` function:

.. sourcecode:: python

    powersof2 = map(lambda x:2 ** x, range(1,11))

    >>> print powersof2
    [2, 4, 8, 16, 32, 64, 128, 256, 512, 1024]

--------------

List comprehension
==================

* Syntactic sugar to easily generate lists
* Syntax for simple comprehension ``[ expression for variable in iterable ]``

Powers of two example with list comprehension:

.. sourcecode:: python

    powersof2 = [ 2 ** x for x in range(1, 11) ]
    >>> print powersof2
    [2, 4, 8, 16, 32, 64, 128, 256, 512, 1024]

--------------

Filtering results
=================

* ``for`` loop method

.. sourcecode:: python

    sentence = "She sells seashells by the seashore"
    wordlist = []
    for word in sentence.split():
        if word.lower().startswith("s"):
            wordlist.append(word)

    print wordlist
    ['She', 'sells', 'seashells', 'seashore']

* Map has a companion, ``filter()``

.. sourcecode:: python

    wordlist = filter(lambda word:word.lower().startswith("s"), sentence.split())
    >>> print wordlist
    ['She', 'sells', 'seashells', 'seashore']

--------------

Comprehension with if clause
============================

* Add a an ``if`` clause to the end of a comprehension to filter results
* Syntax for simple comprehension ``[ expression for variable in iterable if condition ]``

.. sourcecode:: python

    wordlist = [ word for word in sentence.split() if word.lower().startswith("s") ]
    >>> print wordlist
    ['She', 'sells', 'seashells', 'seashore']

--------------

Nested comprehensions
=====================

* List comprehensions can be nested

.. sourcecode:: python

    >>> [ letter * number for number in [1,2,3] for letter in ["a","b","c"]  ]
    ['a', 'b', 'c', 'aa', 'bb', 'cc', 'aaa', 'bbb', 'ccc']

* The order of the ``for`` clauses is significant
* The above is equivalent to:

.. sourcecode:: python

    thelist = []
    for number in [1,2,3]:
        for letter in ["a","b","c"]:
            thelist.append(letter * number)

--------------

More examples
=============

* Convert a list of Celsius temparatures to Fahrenheit

Example from `Python Course`__

.. _PythonCourse: http://www.python-course.eu/list_comprehension.php

__ PythonCourse_

.. sourcecode:: python

    Celsius = [39.2, 36.5, 37.3, 37.8]
    Fahrenheit = [ "%.2f" % ((float(9)/5)*x + 32) for x in Celsius ]
    print Fahrenheit
    ['102.56', '97.70', '99.14', '100.04']

* List of all drive letters in Windows

.. sourcecode:: python

    driveletters = [ "%s:" % letter for letter in string.ascii_uppercase ]
    
    driveletters[:len(driveletters)/2]
    ['A:', 'B:', 'C:', 'D:', 'E:', 'F:', 'G:', 'H:', 'I:', 'J:', 'K:', 'L:', 'M:']
    driveletters[len(driveletters)/2:]
    ['N:', 'O:', 'P:', 'Q:', 'R:', 'S:', 'T:', 'U:', 'V:', 'W:', 'X:', 'Y:', 'Z:']


--------------

More examples 2
===============

* Unique IP addresses from an apache web server log file:

.. sourcecode:: python

    from pprint import pprint

    uniqips = set( [ line.split()[0] for line in open("access.log") ] )

    pprint(list(uniqips)[:5])
    ['180.76.5.65',
     '74.125.19.39',
     '220.181.51.109',
     '123.125.71.75',
     '178.255.215.65']

--------------

Related topics
==============

* For further reading

Generator expressions
  (introduced in Python 2.4)
	http://www.python.org/dev/peps/pep-0289/

Dict comprehensions 
  (introduced in Python 2.7)
	http://www.python.org/dev/peps/pep-0274/

Set comprehensions
  (introduced in Python 2.7)
	http://docs.python.org/release/3.1.5/tutorial/datastructures.html#sets

--------------

Questions?
==========

--------------

Credits
=======
* :Presenter: Shawn K. O'Shea
* :Presented to:  GNHLUG's PySIG
* :Presented on:  July 26, 2012
* :Latest version: You can find the latest version of this presentation on my website: http://eth0.net/
