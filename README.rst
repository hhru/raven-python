About fork
======

This fork only includes debianization instructions.

How to build .deb & upload it to debian repository:

* ``apt-get install python-all debhelper``
* ``pip install --user stdeb``
* configure your ``~/.dput.cf``
* configure your gpg keys
* ``git clone git@github.com:hhru/raven-python.git``
* set postfix for debian version in ``setup.cfg``
* ``cd raven-python``
* ``python setup.py --command-packages=stdeb.command sdist_dsc --with-python2=True --with-python3=True bdist_deb``
* ``cd deb_dist``
* ``debsign python-raven_X.Y.Z-hhN_amd64.changes``
* ``dput hh-apps python-raven_X.Y.Z-hhN_amd64.changes``


Raven
======

.. image:: https://travis-ci.org/getsentry/raven-python.svg?branch=master
    :target: https://travis-ci.org/getsentry/raven-python

Raven is a Python client for `Sentry <http://www.getsentry.com/>`_. It provides
full out-of-the-box support for many of the popular frameworks, including
Django, and Flask. Raven also includes drop-in support for any WSGI-compatible
web application.

Your application doesn't live on the web? No problem! Raven is easy to use in
any Python application.

Resources
---------

* `Documentation <http://raven.readthedocs.org/>`_
* `Bug Tracker <http://github.com/getsentry/raven-python/issues>`_
* `Code <http://github.com/getsentry/raven-python>`_
* `Mailing List <https://groups.google.com/group/getsentry>`_
* `IRC <irc://irc.freenode.net/sentry>`_  (irc.freenode.net, #sentry)
* `Travis CI <http://travis-ci.org/getsentry/raven-python>`_

