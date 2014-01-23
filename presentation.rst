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

:raw-html:`<i class="icon-4x icon-male" style="color: #30A9C5"> </i>`

by Chris McDonough (``@chrismcdonough`` on twitter, ``mcdonc`` on freenode irc)

.. note::

   Thanks for having me here and thank the organizers, particularly Baptiste.
   Sorry for being sick.

   Mostly demo.

----

.. image:: dclogo.jpg

Worked at Digital Creations (aka Zope Corporation) 2000-2003.

----

.. image:: agendaless.png

.. image:: for-hire.jpg

Now a principal of Agendaless Consulting in Fredericksburg, VA, US.

----

.. image:: pyramid-small.png
   :align: left

:raw-html:`<br/>`

.. image:: pylons-small.png
   :align: right

:raw-html:`<br/>`

.. image:: supervisor_logo.gif
   :align: left

:raw-html:`<br/>`

.. image:: repozelogo.gif
   :align: right

.. note::

   Primary author of ``Pyramid`` web framework, ``Supervisor`` UNIX process 
   control system, ``Deform`` form system, ``Colander`` serialization system, 
   ``Repoze``  collection of middleware, and other unmentionables. Maintainer 
   of ``WebOb`` and other stuff that folks have left behind.

----

:raw-html:`<i class="icon-meh icon-4x pull-left" style="color: #30A9C5;"> </i>` Substance D is an
"application server" (let me know if you have a better name).

----

:raw-html:`<i class="icon-file icon-4x pull-left" style="color: #30A9C5;"> </i>`

Developers define "content" (e.g. a blog entry, a product for sale, or a news
item, etc) via plain-old-Python.

----

:raw-html:`<i class="icon-save icon-4x" style="color: #30A9C5;"> </i>`

Content is stored in an object database as a tree.

----

PKD's A Scanner Darkly
======================

.. image:: sdcup.jpg

----


The "SDI"
=========

.. image:: sdi.png

----

:raw-html:`<i class="icon-desktop icon-4x pull-left" style="color: #005F6B"> </i>` 

The SDI allows nonexpert but privileged users to create, edit, update, and
delete developer-defined content.

----

The SDI is a set of views against a hierarchical content space, something like
a filesystem.

:raw-html:`<i class="icon-sitemap icon-4x" style="color: #005F6B"> </i>` 

----

:raw-html:`<i class="icon-lock icon-4x pull-left" style="color:#005F6B"> </i>` 
:raw-html:`<i class="icon-user icon-4x pull-left" style="color:#005F6B"> </i>` 

The SDI also allows for managing less contenty aspects of the
system: users, groups, ACLs, and database connections.

----

:raw-html:`<i class="icon-link icon-4x pull-left" style="color: #005F6B"> </i>` 

The SDI is "real-time"; see content and structure changes as they happen 
without page reloads.


----

The SDI is extensible.  If you can live inside some constraints, you won't need
to write as much admin code.

:raw-html:`<i class="icon-paperclip icon-4x" style="color: #005F6B"> </i>` 

----

Unique Features
===============

----

:raw-html:`<i class="icon-undo icon-4x pull-left" style="color: red"> </i>` 

Undo actions taken via the SDI, or any action invoked against the database
programmatically.

----

:raw-html:`<i class="icon-lock icon-4x pull-left" style="color:red"> </i>` 

Manage hierarchical security declarations attached to content objects.

----

Workflow content.

:raw-html:`<i class="icon-comments icon-4x" style="color:red"> </i>` 


----

:raw-html:`<i class="icon-search icon-4x pull-left" style="color:red"> </i>` 

Indexing and searching of content via field, keyword, 
facet, and full-text indexes.

----

:raw-html:`<i class="icon-magnet icon-4x pull-left" style="color:red"> </i>` 

Relate content objects to each other, with optional
referential integrity.

----

:raw-html:`<i class="icon-fast-forward icon-4x pull-left" style="color:red"> </i>` 

Evolve database content over time as your code changes.

----

:raw-html:`<i class="icon-save icon-4x pull-left" style="color:red"> </i>` 

Dump and load your site's content to/from the filesystem in a mostly
human-readable format.

----

:raw-html:`<i class="icon-copy icon-4x pull-left" style="color:red"> </i>` 

Capture site activity using an audit log.

----

Monitor system performance using built-in hooks.

:raw-html:`<i class="icon-dashboard icon-4x" style="color:red"> </i>` 

----

Run under either Python 2 or Python 3.

----

Demonstrations
==============

Because talks are pretty boring.

.. note::

   - Developers define "content" (e.g. a blog entry, a product for sale, 
     or a news item, etc) via plain-old-Python.  (sdidemo/resources.py)

   - The SDI is a set of views of a hierarchical content space (something like
     a filesystem).  The SDI allows users to create, edit, update, and delete
     developer-defined content.  (sdidemo UI).

   - Views are defined against types.  The URL is a path through a tree plus an
     optional view name.  (@@properties).  Extensibility on two levels:
     adding content extends the URL space without needing to change a routing
     map, adding a type allows you to extend the set of views.  Customers
     who have customers, who have customers.

   - Undo actions taken via the SDI, or any action invoked against the database
     programmatically.  (undo the actions I just took).

   - Content is stored in an object database.  (pshell of sdidev)

   - The SDI also allows for managing less contenty aspects of the
     system: users, groups, and database management. (sdidemo
     database, data evolution, users & groups).

   - SDI is security filtered (sdidemo: protect jimmybob folder with (Allow, 
     admin, sdi.view) and no inherit, log in as "notadmin").  Note hierarchical
     nature and ability to protect a subtree.

   - The SDI is "real-time"; see content and structure changes as they happen
     without page reloads.  (Side by side windows on workspace 2.)

   - Grid can handle many objects (EHN posts view)

   - The SDI is extensible.  (EHN sites/ehn/staging/@@compose_edition view)

   - Capture site activity using an audit log. (Show audit log in sdidev).

   - Built-in performance monitoring hooks. (datadog)

   - Indexing and searching of content via field, keyword, facet, and full-text
     indexes.  (yss.views.song:query).

   - Relate content objects to each other, with optional referential integrity.
     (Song SDI in youshouldsing).

   - Workflow content.  (Agendaless.com workflow)

   - Dump your site's content to the filesystem in a mostly human-readable
     format and reload a dump into the system.  (see kuiu ecommbuildout
     dump).

----

Built With
==========

`ZODB <http://zodb.org>`_

`Pyramid <http://pylonsproject.org>`_

`Hypatia <https://github.com/Pylons/hypatia>`_

`Colander <http://docs.pylonsproject.org/projects/colander/en/latest/>`_

`Deform <http://docs.pylonsproject.org/projects/deform/en/latest/>`_

----

Production Sites
================

----

KUIU
  https://store.kuiu.com

Environmental Health News
  http://www.environmentalhealthnews.org/

The Daily Climate
  http://dailyclimate.org/

----

Release Plan
============

First alpha release date depends on how fast we can address issues in the
Github issue tracker.

----

Development
===========

On GitHub in the Pylons Project
  https://github.com/Pylons/substanced

News/FAQ/docs
  http://substanced.net

----

:raw-html:`<i class="icon-question-sign icon-4x" style="color:red"> </i>` 

