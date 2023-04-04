

.. _steps_needed:

.. _installation:

Installation
=============

To deploy this guide from `coderrefinery <https://coderefinery.github.io/documentation/gh_workflow/>`_ , follow these steps...

**1. Install support packages from terminal.**

.. code-block:: python

   pip install sphinx_rtd_theme
   pip install sphinx_copybutton
   pip install myst_parser
   pip install sphinx_design
   pip install pip install myst-nb

| - Sphinx_rtd_theme is the current blue and yellow theme provided by 'ReadtheDocs'.
| - Copybutton allows us to copy code from code blocks.
| - Myst_parser allows us to use markdown instead of rst.
|   Myst parser comes with its own extensions, such as Code and 'Colon Fence' for Admonitions.
| - Sphinx_design allow for use of grids and cards in a document.
| - Myst_NB allows for integration of Jupyter Notebook `Myst-nb <https://myst-nb.readthedocs.io/en/v0.9.0/use/start.html>`_

| **2.** Modify **CONF.PY**
|     2a. After generating the template, in Conf.py, set the language.

.. code-block:: python

   language = en

|     **2b.** Modify **conf.py**, look for **'html_theme'** and add:

.. code-block:: python

   html_theme = 'sphinx_rtd_theme'

.. image:: /Images/change_theme.png

####

| **2c.**
| Look for:
| '# -- General configuration ------------------------------------------------'
| and enable all pip installed extensions.

.. code-block:: python

    extensions = [
                  'sphinx.ext.autodoc',
                  'sphinx_copybutton',
                  'sphinx.ext.autosectionlabel',
                  'myst_parser',
                  'sphinx_design'
                 ]

    myst_enable_extensions = [
                              "colon_fence",
                              "html_image"
                             ]


| **4c. Seperately, enable myst extensions, as shown above.**

**4. Add and Update .yml file for gitpages.**

| Create a workflow/yaml file. This can be done in our repo using the 'add' file button.
| or we can do so locally.

.. code-block:: python

    .github/workflows/docmentation.yaml

.. image:: /Images/workflow-yaml.png

The contents of the yaml file must include commands to install the extensions.

.. code-block:: python

            name: Docs
        on: [push, pull_request, workflow_dispatch]
        permissions:
            contents: write
        jobs:
          docs:
            runs-on: ubuntu-latest
            steps:
              - uses: actions/checkout@v3
              - uses: actions/setup-python@v3
              - name: Install dependencies
                run: |
                  pip install sphinx sphinx_rtd_theme
                  pip install myst-parser
                  pip install sphinx_copybutton
                  pip install sphinx_design
              - name: Sphinx build
                run: |
                  sphinx-build doc _build
              - name: Deploy
                uses: peaceiris/actions-gh-pages@v3
                if: ${{ github.event_name == 'push' && github.ref == 'refs/heads/main' }}
                with:
                  publish_branch: gh-pages
                  github_token: ${{ secrets.GITHUB_TOKEN }}
                  publish_dir: _build/
                  force_orphan: true


Above, we see that there is a 'pip install extension' command for every extension we deploy.

.. attention:: Warning:
    Mac Machines hide files starting with '.'

To make the invisible, visible, enter the following into the terminal.

.. code-block:: python

    Type defaults write com.apple.Finder AppleShowAllFiles true
    Type killall Finder


####

.. In essence these will act as subsections.

Build
~~~~~

This is the command to build using Coderefinery's setup.

.. code-block:: python

   sphinx-build doc _build


**Test HTML pages links**

Inside the cloned repository, check the integrity of all internal and external links:

.. code-block::

    sphinx-build doc -W -b linkcheck -d _build/doctrees _build/html





