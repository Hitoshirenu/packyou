packyou
=======

|Build Status| |Code Health| |Coverage Status|

Description
-----------

Downloads a python project from github and allows to import it from
anywhere. Very useful when the repo is not a package

Demo
----

.. figure:: https://cloud.githubusercontent.com/assets/568181/18405569/63b0cf9e-76c9-11e6-845e-594101c36136.gif
   :alt: 

Introduction
------------

Sometimes is usefull to be able to import a project from github. If the
project is configured as a python package it could be installed with pip
and git. But still lot of project are not using setuptools which makes
difficult to use them from python easily. Some people could be using git
submodules, but it also requires adding a **init**.py file in the
project root.

With packyou it is possible to import any pure python project from
github justo with a simple import statement like:

.. code:: python

    from packyou.github.username.repository_name import external_github_module

Install
-------

::

    pip install packyou

Example of usage
----------------

Supose you want to use something from sqlmap project. since sqlmap
proyect is not yet a python package you can import anything from sqlmap
like this:

.. code:: python

    from packyou.github.sqlmapproject.sqlmap.lib.utils.hash import mysql_passwd
    mysql_passwd(password='testpass', uppercase=True)
    # '*00E247AC5F9AF26AE0194B41E1E769DEE1429A29'

screenshot!

-  Free software: MIT license
-  Documentation: https://packyou.readthedocs.io.

TODO
-----------
- Add support for bitbucket, gitlab
- Specify version of each project

.. |Build Status| image:: https://travis-ci.org/llazzaro/packyou.svg?branch=master
   :target: https://travis-ci.org/llazzaro/packyou
.. |Code Health| image:: https://landscape.io/github/llazzaro/packyou/master/landscape.svg?style=flat
   :target: https://landscape.io/github/llazzaro/packyou/master
.. |Coverage Status| image:: https://coveralls.io/repos/github/llazzaro/packyou/badge.svg?branch=master
   :target: https://coveralls.io/github/llazzaro/packyou?branch=master




