

.. _Learning

LEARNING
========

####

.. note:: How to Escape Special Characters

   \* Back Slash to Escape Special Characters.

.. attention:: Build Command:
   **sphinx-build doc _build**

   This is the command to build instead of 'make'.

Header Sizes
============

####

##################
H1: document title
##################

Introduction text.


*********
Sample H2
*********

Sample content.


**********
Another H2
**********

Sample H3
=========

Sample H4
---------

Sample H5
^^^^^^^^^

Sample H6
"""""""""

1. The largest Header size is designated by underlining the header with:

.. code-block:: python

   ====


ie. HEADER
==========
\_____________________

2. The second size Header is designated by four or more dashes - - - - :

.. code-block:: python

   -----



3. The third size Header is designated by four or more tildes ~ ~ ~ ~ :

.. code-block:: python

   ~~~~



To create a line across the page use:

.. code-block:: python

   #### or - - - - with no spaces.


\_____________

**Alternate Method of bolding:**

.. note:: Note:
   Indenting four equals '= = = =' signs, yields a bolding of the text. See below.

.. image:: ./Images/indent_equals.png

'Code block ends'
      ====

This is comparable to using \** \** for bolding as seen below:

**'Code block ends'**

####
.. _CodeBlocks
Code Blocks
============

.. code-block:: python
   :linenos:

   .. code-block:: python
      :linenos:

      def hello():
       print("Hello, world!")

.. note::
   We do not need to escape special characters in code-blocks. ':linenos:' adds lines and needs opens and closes with : :

####

Embed an image:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: python

   .. image:: ./Images/EmbedImages.png
      :width: 400px
      :align: left


.. image:: ./Images/EmbedImages.png
   :width: 600px
   :align: center

.. // if we don't use align: center, the text below windows the picture.
| Using directories:
.. code-block:: python

   .. image:: ./Images/EmbedImages.png

####

This is the :ref: `target page <target>` for more information.

Links
=====

Links to Sections in the Same Document
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:ref: `Code Blocks`

:ref:`Code Blocks`

code blocks:

:role:`CodeBlocks`


How to Link to other pages.
~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Define Reference text.

.. code-block:: python

   :ref:`link text <document_name:section_label>`


.. code-block:: python

   :doc:`link text <document_name>`


2. Define the Target page.

.. code-block:: python

   .. _target:
   Target Page
   ===========
   This is the target page.


This is a sentence that will :doc: `reference usage <usage.rst>`_

.. note::
    Intersphinx is an extension for links between different projects.

####

Comments
~~~~~~~~

Comments are preceded with dot, dot '. . ' at the beginning of the line.

.. code-block::

   ..

####

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

| From the tutorial `coderefinery <https://coderefinery.github.io/documentation/gh_workflow/>`_ we do not use 'make' but instead use:

.. code-block:: python

    sphinx-build doc _build

This tutorial uses the theme **'sphinx_rtd_theme'**:

.. code-block:: python

    1. pip install sphinx_rtd_theme
    2. In Conf.py, add: html_theme = 'sphinx_rtd_theme'

.. This is another example of line block, aka carriage return.

Line block serves as line wrap
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Use the character ' | ' at the beginning of all sentences. Be sure to add a space after \ .

.. code-block::

   | Line block
   | New line and we are still on

| Line block
| New line and we are still on
  the same line
|   Yet a new line

Please see the :ref:`installation instructions <installation>` for more information.

To Change the Indent in Pycharm
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: python

   1. File > Settings (on Windows and Linux) or PyCharm > Preferences (on Mac).
   2. Select Editor > Code Style > Python.
   3. In the Tabs and Indents tab, change the Tab size and Indent options to 3.





v3