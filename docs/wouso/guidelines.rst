Guidelines
==========

Coding style
------------

* set ts=4
* import order::

    import <python-modules>
    import <django-modules>
    import <wouso.[core|interface]>
    import <game-modules>

Logging
-------

log everything
see Logging

Testing
-------

Always write unit tests for your code, see Scoring or Qotd for examples. The example
configuration file uses `nose` as the test runner. To run the full test
suite for WoUSO::

    ./manage.py test

Documentation
-------------

WoUSO documentation is maintained using Sphinx_ in the repository, under
``/docs/wouso``. To update it:

* Edit a page::

    cd docs
    vim guidelines.rst

* Build locally::

    make html

* Check the generated HTML. It's under ``_build/html``.

* Upload to publc server::

    rsync -rv --del _build/html/ wouso@rosedu.org:public_html/docs

.. _Sphinx: http://sphinx.pocoo.org/
