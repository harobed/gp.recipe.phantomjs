Supported options
=================

The recipe supports the following options:

.. Note to recipe author!
   ----------------------
   For each option the recipe uses you should include a description
   about the purpose of the option, the format and semantics of the
   values it accepts, whether it is mandatory or optional and what the
   default value is if it is omitted.

phantomjs-url
    Url to download phantomjs

casperjs-url
    Url to download casperjs


Example usage
=============

We'll start by creating a buildout that uses the recipe::

    >>> write('buildout.cfg',
    ... """
    ... [buildout]
    ... parts = casperjs
    ...
    ... [casperjs]
    ... recipe = gp.recipe.phantomjs
    ... """)

    >>> _ = system('buildout')

    >>> ls('bin')
    -  buildout
    -  casperjs
    -  phantomjs

