.. highlight:: shell

=========
New index
=========

The index calculation is based on xclim_. Index calculator only calculated indices, which are available in xclim. If you need an index, which is not included in xclim, please integrate it in xclim not here.

First, if you need a new index you need to edit two files:

.. code-block:: console

    $ cd index_calculator/tables
    $ input_vars.json
    $ metadata.json

In input_vars.json, add the name of the new index and the input parameter it needs.
In metadata.json, add a block similar to the existing, providing all metadata for your new index (copy metadata from xclim)

Second:

.. code-block:: console

    $ cd index_calculator/
    $ emacs _indices.py


The easiest way is to copy an exsiting index which is similar to your new one and adjust it to your needs. The naming conventions can de found in xclim_ under indicators (not indices).

At last you need to perform a test:

.. code-block:: console

    $ pip install pytest


Please edit test_indices.py in the tests directory and execute

.. code-block:: console

    $ cd tests
    $ test_indices.py (edit)
    $ pytest (run)




.. _xclim: https://github.com/Ouranosinc/xclim
