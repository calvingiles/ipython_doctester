=================
ipython_doctester
=================

Lets you run the doctests of a single class or function at a time.  Useful for 
tutorials based on the IPython Notebook, using doctests for student feeback.

Install with ``pip install ipython_doctester``, or 
navigate to this directory and run::

    python setup.py install

Use
===

Run ``ipython notebook``, then start your notebook with this import::

    In [1]: from ipython_doctester import test

In each subsequent cell, set up objects with their doctests, and with absent 
(or flawed) function bodies, and decorate them with @test::

    In [2]: @test
            def square(x):
                '''
                >>> f(2)
                4
                '''
                
Tests will run on each cell as it is executed.

Only change to original so far is to silence the success output for non-teaching applications.

Development
===========

https://github.com/calvingiles/ipython_doctester

Thanks to
=========

This is a fork from Catherine Devlin. Thanks to her for the original project and to Brian Granger for original technical advice
