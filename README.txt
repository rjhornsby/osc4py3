OSC for Python3
===============

2021-Feb-10 github.com/rjhornsby
 * Forked from author's SVN, https://sourcesup.renater.fr/projects/osc4py3/
 * Fixed minor typo in oscscheduling.py

Original README content below without modification.

:author: Laurent Pointal <laurent.pointal@limsi.fr> <laurent.pointal@laposte.net>
:organization: CNRS - LIMSI
:copyright: CNRS - 2013-2018
:license: CeCILL-2.1
:version: 1.0.8


`Module documentation <http://osc4py3.readthedocs.org/>`_

`Subversion repository & bug tracking <https://sourcesup.renater.fr/scm/viewvc.php?root=osc4py3>`_
(on french academic SourceSup site).

`Developer page <https://perso.limsi.fr/pointal/dev:osc4py3>`_

.. note::

    Testers feedback welcome. This development was finally not tested in its
    initial planning, any problem / bug / info are welcome.

What is it?
-----------

This module is an implementation of `Open Sound Control (OSC)`_ message
transport protocol within a Python3 package.

.. _Open Sound Control (OSC): http://opensoundcontrol.org/

Manage different sides of OSC in possibly different contexts:

- encoding/decoding of OSC message packets (including bundles)
- routing of incoming messages based on selector regexps or globbing
- timed messages with possible delay period
- named client/server for sending/subscribing
- different scheduling models (single process, totally multithread, only multithread for communications)
- extra processing of packets (hack points to encrypt/decrypt, sign/verify…)

Note: routing, timed messages, named client/server, scheduling models make a complex system
(see the “big picture” in doc). The oscbuildparse module of osc4py3 package can be used as
is and provides nice OSC packets encoding/decoding functions usable in your own message
transmission scheme.



Installation
------------

Unless someone built a package for your OS distro, the simplest procedure
is to use ``pip`` to install the module:

    pip install osc4py3

If you have no admin access to install things on you computer, you may install
a virtualenv and run pip inside this virtual env, or you can do a local user
installation:

    pip install --user osc4py3

