.. include:: <s5defs.txt>

Substance D
===========

:Authors: Chris McDonough, Agendaless Consulting
:Date: 06/02/2013 (DCPython)

..  footer:: Chris McDonough, Agendaless Consulting

Who Am I
--------

Came to Python via Zope in 1999.  Worked at Digital Creations (aka Zope
Corporation) until 2003.  Now a consultant with Agendaless Consulting.

Primary author of Pyramid web framework, Supervisor UNIX process control
system, Deform form system, Repoze collection of middleware, and other
unmentionables.  Contributor to Zope, WebOb, and other OSS projects.

A Scanner Darkly
-----------------

.. raw:: html

   <center>
      <div style="padding-bottom: 20px; padding-top: 20px;">PKD was my kind of guy!</div>
      <iframe width="560" height="315" src="http://www.youtube.com/embed/eLeC28enMr0" frameborder="0" allowfullscreen></iframe>
   </center>

.. class:: handout

   http://www.youtube.com/watch?v=eLeC28enMr0

Features
--------

Substance D is an application server.  It provides the following features:

- Facilities that allow developers to define "content" (e.g. "a blog entry", "a
  product", or "a news item", etc).

- A management (aka "admin") web UI which allows nonexpert but privileged users
  to create, edit, update, and delete developer-defined content as well as
  managing other aspects of the system such as users, groups, security, etc.

Features (2)
------------

- "Undo" capability for actions taken via the management UI.

- A way to make granular hierarchical security declarations for content
  objects. "Bob can edit *this* post" or "Bob can edit all posts in this
  collection" as opposed to just "Bob can edit posts".

- Built-in users and groups management.

Features (3)
------------

- Built-in content workflow.

- Indexing and searching of content (field, keyword, facet, and full-text).

- A facility for relating content objects to each other (with optional
  referential integrity).

Features (4)
------------

- An "evolve" mechanism for evolving content over time as it changes.

- A mechanism to dump your site's content to the filesystem in a mostly
  human-readable format, and a mechanism to reload a dump into the system.

- An audit log for high security environments.

Built On
--------

Substance D is built upon on the following technologies:

- `ZODB <http://zodb.org>`_

- `Pyramid <http://pylonsproject.org>`_

- `hypatia <https://github.com/Pylons/hypatia>`_

- `colander <http://docs.pylonsproject.org/projects/colander/en/latest/>`_

- `deform <http://docs.pylonsproject.org/projects/deform/en/latest/>`_

Relationship with Zope
----------------------

- Substance D is effectively a reimplementation of Zope 2.  Its user interface
  and content storage model is heavily influenced by Zope 2's.

- It, howevever, shares no DNA with Zope, save for ZODB.  It's a "from scratch"
  effort.  It outsources all of its low-level routing functionality to Pyramid
  (Zope doesn't have an equivalent base layer).

- Zope does things that Substance D does not: "through the web" development,
  omnipresent WebDAV, omnipresent XML-RPC.  These may become available as
  add-ons to Substance D later (although more likely the latter 2 than the
  first).

Is It A CMS?
------------

- Who knows.  Maybe not a useful term.  I've been doing "CMS" for ~ 12 years
  and I don't really know what CMS means.  Apparently some sites don't have any
  content?

- If your site is dynamic, you can use Substance D to create it.  Particularly
  if you can naturally think of your data as treelike.

Production Sites
----------------

- KUIU:  https://store.kuiu.com

- Environmental Health News: http://www.environmentalhealthnews.org/

Contact Info
------------

Chris McDonough, Agendaless Consulting

chrism@agendaless.com

@chrismcdonough on Twitter

"mcdonc" on Freenode IRC
