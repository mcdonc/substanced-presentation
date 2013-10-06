:title: Substance D
:author: Chris McDonough
:description: Introduction to the Substance D Web Application Server
:keywords: substanced, web framework:
:css: hovercraft.css
:data-transition-duration: 1500

.. role:: raw-html(raw)
   :format: html

My Substance D presentation

----

Substance D
===========

.. image:: capsule-icon-128.png

A civilized way to build web applications.
------------------------------------------

----

Who Am I
========

Came to Python 1999.  Worked at Digital Creations (aka Zope
Corporation) until 2003.  Now a principal of Agendaless Consulting in
Fredericksburg, VA, US.

----

Primary author of ``Pyramid`` web framework, ``Supervisor`` UNIX process 
control system, ``Deform`` form system, ``Colander`` serialization system, 
``Repoze``  collection of middleware, and other unmentionables.  Maintainer 
of ``WebOb`` and other stuff that folks have left behind.

----

A Scanner Darkly
================

.. raw:: html

   <center>
      <div style="padding-bottom: 20px; padding-top: 20px;">PKD was my kind of guy!</div>
      <iframe width="560" height="315" src="http://www.youtube.com/embed/oVnvilLFk2Y" frameborder="0" allowfullscreen></iframe>
   </center>

.. class:: note

   http://www.youtube.com/watch?v=eLeC28enMr0

----

Substance D is an "application server" (anybody have a better name?).

----

Allows developers to define "content" (e.g. "a blog entry", "a
product", or "a news item", etc) via plain old Python.

----

The "SDI" (Substance D Interface):

.. image:: sdi.png

----

:raw-html:`<i class="icon-camera-retro icon-4x pull-left"> </i>` The SDI is a management (aka 
"admin") web UI which allows nonexpert but privileged users to create, edit, 
update, and delete developer-defined content.

----

The SDI is a view of a hierarchical content space, something like a filesystem.

----

The SDI also allows for managing slightly less "contenty" aspects of the system 
such as users, groups, ACLs, and database connections.

----

The SDI is "real-time"; you see content and structure changes as they happen 
without any page reloads.

----

Unique Features
===============

----

There is an "Undo" capability for actions taken via the SDI, or any action
invoked against the database programmatically.

----

You can manage hierarchical security declarations attached to content objects.

----

Substance D provides content workflow.

----

Substance D provides indexing and searching of content via field, keyword, 
facet, and full-text indexes.

----

A facility exists for relating content objects to each other, with optional
referential integrity.

----

An "evolve" mechanism allows you to evolve database content over time as 
your code changes.

----

A dump facility pushes your site's content to the filesystem in a mostly
human-readable format.  A load mechanism allows you to to reload a dump into 
the system.

----

An audit log feature exists for high security environments.

----

Substance D runs under either Python 2 or Python 3.

----

Demonstrations
==============

Because talks are pretty boring.

----

Built With
==========

`ZODB <http://zodb.org>`_

`Pyramid <http://pylonsproject.org>`_

`hypatia <https://github.com/Pylons/hypatia>`_

`colander <http://docs.pylonsproject.org/projects/colander/en/latest/>`_

`deform <http://docs.pylonsproject.org/projects/deform/en/latest/>`_

----

Relationship with Zope
======================

----

"Seriously?  The Z word?  You're going there huh?"

----

Substance D is effectively a reimplementation of Zope 2.  Its user interface
and content storage model is heavily influenced by Zope 2's.

----

It, howevever, shares no DNA with Zope, save for ZODB.  It's a "from scratch"
effort.  It outsources all of its low-level routing functionality to Pyramid
(Zope doesn't have an equivalent base layer).

----

Zope does things that Substance D does not.  For example, Zope allows for 
"through the web" development.  Substance D does not.

----

Is It A CMS?
============

----

Who knows.  Maybe not a useful term.  I've been doing "CMS" for ~ 12 years
and I don't really know what CMS means.  Apparently some sites don't have any
content?

----

If your site is dynamic, you can use Substance D to create it.  Particularly
if you can naturally think of your data as treelike.

----

Plans
=====

A release!  Currently there is none.

Release date mostly depends on how fast we can address issues in the Github
issue tracker.

----

Development
===========

On GitHub in the Pylons Project: https://github.com/Pylons/substanced

News/FAQ/docs via http://substanced.net

----

Production Sites
================

KUIU
  https://store.kuiu.com

Environmental Health News
  http://www.environmentalhealthnews.org/

The Daily Climate
  http://dailyclimate.org/

