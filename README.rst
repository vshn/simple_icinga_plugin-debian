********************
simple_icinga_plugin
********************

a simple icinga plugin helper module, providing a few common methods,
regularily used in icinga/nagios plugins.

============
Installation
============

.. code-block:: bash

    $ pip install simple_icinga_plugin


================
Package Building
================

PyPI
====

.. code-block:: bash

    # Install setuptools, twine and wheel dependencies
    $ python3 setup.py sdist
    $ python3 setup.py bdist_wheel
    $ twine upload dist/simple_icinga_plugin-*

Debian
======

.. code-block:: bash

    $ git clone git@github.com:vshn/simple_icinga_plugin-debian.git
    $ cd simple_icinga_plugin-debian
    $ git checkout upstream
    $ git checkout master
    $ git-import-orig ../simple_icinga_plugin-VERSION.tar.gz 
    $ dch -v VERSION-1 -D trusty 'New upstream release.'
    $ git commit -am 'New upstream release.'
    $ git-buildpackage -S --git-tag
    $ git push --all
    $ git push --tags

Redhat
======

.. code-block:: bash

    # Install python34-setuptools python34
    $ git clone git@github.com:vshn/simple_icinga_plugin.git
    $ python3 setup.py bdist_rpm

