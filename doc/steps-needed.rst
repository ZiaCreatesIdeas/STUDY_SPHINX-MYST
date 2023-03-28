

.. _steps_needed:

.. _installation:

Installation
=============

To deploy this guide from `coderrefinery <https://coderefinery.github.io/documentation/gh_workflow/>`_ , follow these steps...

1. After generating the template, in Conf.py, set the language.

.. code-block:: python

   language = en

2. Install the sphinx_rtd_theme.

.. code-block:: python

   pip install sphinx_rtd_theme

2b. Modify **conf.py**:

.. code-block:: python

   html_theme = 'sphinx_rtd_theme'

.. image:: /Images/change_theme.png

####

.. In essence these will act as subsections.


**Test HTML pages links**

Inside the cloned repository, check the integrity of all internal and external links:

.. code-block::

    sphinx-build doc -W -b linkcheck -d _build/doctrees _build/html





