Welcome to Django Tasker Exchange Rate documentation!
=====================================================

.. image:: https://travis-ci.org/kostya-ten/django_tasker_exchangerate.svg?branch=master
    :target: https://travis-ci.org/kostya-ten/django_tasker_exchangerate

.. image:: https://readthedocs.org/projects/django-tasker-exchange-rate/badge/?version=latest
    :target: https://django-tasker-exchange-rate.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status



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

Using
""""""
.. code-block:: python

    from django_tasker_exchangerate import exchangerate
    exchange = exchangerate.CBRF()
    model = exchange.model()
    result = model.objects.get(last=True, code="USD")
    print(result.value)

Update
""""""
You can update the exchange rate using cron

.. code-block:: bash

    14   00   *   *   *   root    test -x manage.py && manage.py exchangerate --action=cbrf