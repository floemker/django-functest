============
Contributing
============

Contributions are welcome, and they are greatly appreciated! Every little bit
helps, and credit will always be given.

You can contribute in many ways:

Types of Contributions
----------------------

Report Bugs
~~~~~~~~~~~

Report bugs at https://github.com/django-functest/django-functest/issues.

If you are reporting a bug, please include:

* Your Django version.
* Browser name and version if applicable.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

Fix Bugs
~~~~~~~~

Look through the GitHub issues for bugs. Anything tagged with "bug"
is open to whoever wants to implement it.

Implement Features
~~~~~~~~~~~~~~~~~~

Look through the GitHub issues for features. Anything tagged with "feature"
is open to whoever wants to implement it.

Write Documentation
~~~~~~~~~~~~~~~~~~~

django-functest could always use more documentation, whether as part of the
official django-functest docs, in docstrings, or even on the web in blog posts,
articles, and such.

Submit Feedback
~~~~~~~~~~~~~~~

The best way to send feedback is to file an issue at https://github.com/django-functest/django-functest/issues

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that this is a volunteer-driven project, and that contributions
  are welcome :)

Get Started!
------------

Ready to contribute? Here's how to set up `django-functest` for local development.

1. Fork the `django-functest` repo on GitHub.
2. Clone your fork locally::

    $ git clone git@github.com:your_name_here/django-functest.git

3. Install your local copy into a virtualenv. Assuming you have virtualenvwrapper installed, this is how you set up your fork for local development::

    $ mkvirtualenv django-functest
    $ cd django-functest/
    $ python setup.py develop

4. Create a branch for local development::

    $ git checkout -b name-of-your-bugfix-or-feature

Now you can make your changes locally.

5. When you're done making changes, check that your changes pass flake8 and the
tests, including testing other Python versions with tox::

    $ flake8 django_functest
    % isort -rc -c .
    $ ./runtests.py
    $ tox

To get flake8/tox/isort, just pip install them into your virtualenv.

To run the full test suite, you will need to install:

* Firefox

  Currently the latest version of Firefox that can be reliably used
  for Selenium tests is Firefox 45.

  With Firefox 50 and later, you can use geckodriver
  https://github.com/mozilla/geckodriver with Selenium 3, but this appears to
  be very incomplete.

  Alternatively you can get Firefox 45 here -
  https://www.mozilla.org/en-US/firefox/organizations/all/
  You may be able to extract it without installing over other versions of Firefox.

  To use it in tests, use the ``--firefox-binary`` to ``runtests.py``

* `chromedriver <https://sites.google.com/a/chromium.org/chromedriver>`_

* `PhantomJS <http://phantomjs.org/>`_.

6. Commit your changes and push your branch to GitHub::

    $ git add .
    $ git commit -m "Your detailed description of your changes."
    $ git push origin name-of-your-bugfix-or-feature

7. Submit a pull request through the GitHub website.

Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests.
2. If the pull request adds functionality, the docs should be updated. Put
   your new functionality into a function with a docstring, and add the
   feature to the list in README.rst.
3. The pull request should work for Python 2.7, 3.3, 3.4 and 3.5. Check
   https://travis-ci.org/django-functest/django-functest/pull_requests
   and make sure that the tests pass for all supported Python versions.

Tips
----

To run a subset of tests::

    $ ./runtests.py  django_functest.tests.SomeTestCase

Conduct
-------

Contributors of any kind are expected to act with politeness to all other
contributors, in pull requests, issue trackers etc., and harassing behaviour
will not be tolerated.
