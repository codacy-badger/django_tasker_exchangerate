Welcome to Django Tasker Exchange Rate documentation!
=====================================================

Requirements
""""""""""""""""""
* Python 3.6+
* A supported version of Django (currently 2.2.4)

Getting It
""""""""""""""""""

You can get Django Tasker Exchange Rate by using pip::

    $ pip install django-tasker-exchangerate

If you want to install it from source, grab the git repository from GitHub and run setup.py::

    $ git clone git://github.com/kostya-ten/django_tasker_exchangerate.git
    $ cd django_tasker_exchangerate
    $ python setup.py install

Installation
""""""""""""""""""
To enable ``django_tasker_exchangerate`` in your project you need to add it to `INSTALLED_APPS` in your projects ``settings.py``

.. code-block:: python

    INSTALLED_APPS = (
        # ...
        'django_tasker_exchangerate',
        # ...
    )
