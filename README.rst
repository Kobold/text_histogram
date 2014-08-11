`text_histogram`_ |version| |downloads|
=======================================

Histograms are great. This is `Bit.ly's data_hacks
<https://github.com/bitly/data_hacks>`_ histogram.py repackaged for convenient
script use.

::

    >>> from text_histogram import histogram
    >>> import random
    >>> histogram([random.gauss(50, 20) for _ in xrange(100)])
    # NumSamples = 100; Min = 1.42; Max = 87.36
    # Mean = 51.848095; Variance = 332.055832; SD = 18.222399; Median 53.239251
    # each ∎ represents a count of 1
        1.4221 -    10.0159 [     3]: ∎∎∎
       10.0159 -    18.6098 [     3]: ∎∎∎
       18.6098 -    27.2036 [     6]: ∎∎∎∎∎∎
       27.2036 -    35.7974 [     4]: ∎∎∎∎
       35.7974 -    44.3913 [    17]: ∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
       44.3913 -    52.9851 [    16]: ∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
       52.9851 -    61.5789 [    17]: ∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
       61.5789 -    70.1728 [    20]: ∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
       70.1728 -    78.7666 [     8]: ∎∎∎∎∎∎∎∎
       78.7666 -    87.3604 [     6]: ∎∎∎∎∎∎


Installation
============

.. code:: bash

    $ pip install data_hacks

Why?
====

Histograms are great for exploring data, but numpy and matplotlib are heavy and
overkill for quick analysis. They also can't be easily used on remote servers or
over ssh. Don't even get me started on installing them.

`data_hacks`_ is pretty great, but difficult to use from python code directly
because it requires an ``optparse.OptionParser`` to pass histogram options.

.. _data_hacks: https://github.com/bitly/data_hacks
.. _text_histogram: https://github.com/Kobold/text_histogram

.. |downloads| image:: https://pypip.in/d/text_histogram/badge.png
   :target: https://pypi.python.org/pypi/text_histogram
   :alt: Number of PyPI downloads
.. |version| image:: https://badge.fury.io/py/text_histogram.png
   :target: http://badge.fury.io/py/text_histogram
   :alt: PyPI version
