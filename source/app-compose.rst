compose
*******

.. highlight:: html

https://github.com/pkimber/compose

The ``compose`` app extends the :doc:`app-block` app and allows an
administrator to create new pages and sections.

Compose
=======

Article
-------

See the template in ``compose/page_article.html``.  This is used by the home
page of the example app.

Feature
-------

Provides a page section with a title, description and a picture

See the template ``compose/page_feature.html`` (this uses the
``compose/_event_feature.html`` snippet which displays events using the feature
block).

This page is not created when the ``example_cms`` app is initialised so you
need to log in to the ``example_cms`` app as ``admin`` and follow this
procedure to configure it.

.. note:: Please note this page also uses a header block so you need to
          configure it (see the section below).

Create a section (*Dashboard* | *Section*)::

  Name          Feature A
  Slug          feature_a
  Block app     compose
  Block model   Feature
  Create url    compose.feature.create

Create a template called ``compose/page_feature.html`` (*Dashboard* |
*Template*).  Add the *Feature A* section created above.

Create a Feature style called ``Event`` css class ``event`` (*Settings* |
*Feature Styles*)

Create a page that uses the ``page_feature`` template (*Dashboard* | *Create
Page*)

You can now manage the content on this page using design mode.

Header
------

Provides a page section that displays a header.

See the template ``page_feature.html``.  In addition to the steps above...

Create a section (*Dashboard* | *Section*)::

  Name          Header A
  Slug          header_a
  Block app     compose
  Block model   Header
  Create url    compose.header.create

Add this section to the template ``compose/page_feature.html`` created above
(*Dashboard | *Template*)

You can now manage the content on this page using design mode.