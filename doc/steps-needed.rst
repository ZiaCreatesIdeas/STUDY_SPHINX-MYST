

.. _steps_needed:

.. _installation:

Installation
=============

To deploy this guide from `coderrefinery <https://coderefinery.github.io/documentation/gh_workflow/>`_ , follow these steps...

1. In Conf.py, set the language.

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

Learning
========
####

.. note:: How to Escape Special Characters

   \* Back Slash to Escape Special Characters.

.. attention:: Build Command:
   **sphinx-build doc _build**

   This is the command to build instead of 'make'.

Header Sizes
~~~~~~~~~~~~

1. The largest Header size is designated by underlining the header with:

.. code-block:: python

   ====


ie. HEADER
==========


2. The second size Header is designated by four or more dashes - - - - :

.. code-block:: python

   -----



3. The third size Header is designated by four or more tildes ~ ~ ~ ~ :

.. code-block:: python

   ~~~~



To create a line across the page use:

.. code-block:: python

   ####

Yields:

####


.. note:: Note:
   Indenting four equals '= = = =' signs, yields a bolding of the text. See below.

.. image:: ./Images/indent_equals.png

'Code block ends'
      ====

This is comparable to using \** \** for bolding as seen below:

**'Code block ends'**

####

Code block example:
~~~~~~~~~~~~~~~~~~~~

.. code-block:: python
   :linenos:

   def hello():
       print("Hello, world!")


This is an example of an embedded image:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: ./Images/EmbedImages.png
.. :width: 400px
.. :align: center

Using directories:

.. code-block:: python

   .. image:: ./Images/EmbedImages.png


This is the :ref: `target page <target>` for more information.

How to Link to other pages.
~~~~~~~~~~~~~~

1. Define Reference text.

.. code-block:: python

   :ref:`link text <document_name:section_label>`
   :doc:`link text <document_name>`



2. Define the Target page.

.. code-block:: python

   .. _target:
   Target Page
   ===========
   This is the target page.

.. note::
   Comments use two periods at the start '. .'
   \.. this is a comment.

.. COPY BUTTON ..

How to Add a Copy Button to Code Blocks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: /Images/copy_button/copy_button_01.png
.. :align: center

.. image:: /Images/copy_button/copy_button_02.png
.. :align: center

.. image:: /Images/copy_button/copy_button_03.png
.. :align: center

.. image:: /Images/copy_button/copy_button_04.png
.. :align: center

.. image:: /Images/copy_button/copy_button_05.png
.. :align: center


This is a :strong:`bold` word.


.. Both lines have to have the line | block element.

| This is the command to build using the tutorial at:
| `coderefinery <https://coderefinery.github.io/documentation/gh_workflow/>`_

.. code-block:: python

    sphinx-build doc _build

This tutorial uses the theme 'sphinx_rtd_theme':

.. code-block:: python

    pip install sphinx_rtd_theme

.. This is another example of line block, aka carriage return.

| Line block
| New line and we are still on
  the same line
|   Yet a new line

Please see the :ref:`installation instructions <installation>` for more information.

To Change the Indent in Pycharm:
-------------------------------

* Open PyCharm and go to File > Settings (on Windows and Linux) or PyCharm > Preferences (on Mac).
* In the left-hand panel, select Editor > Code Style > Python.
* In the Tabs and Indents tab, change the Tab size and Indent options to 3.
* Click Apply and OK to save the changes.



Here we have a line of text just for separation.





v3


