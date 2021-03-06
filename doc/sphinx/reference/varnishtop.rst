==========
varnishtop
==========

-------------------------
Varnish log entry ranking
-------------------------

:Author: Dag-Erling Smørgrav
:Author: Martin Blix Grydeland
:Date:   2010-05-31
:Version: 1.0
:Manual section: 1



SYNOPSIS
========

.. include:: ../../../bin/varnishtop/varnishtop_synopsis.rst
varnishtop |synopsis|

DESCRIPTION
===========

The varnishtop utility reads ``varnishd(1)`` shared memory logs and
presents a continuously updated list of the most commonly occurring
log entries.  With suitable filtering using the ``-I``, ``-i``, ``-X``
and ``-x`` options, it can be used to display a ranking of requested
documents, clients, user agents, or any other information which is
recorded in the log.

The following options are available:

.. include:: ../../../bin/varnishtop/varnishtop_options.rst

EXAMPLES
========

The following example displays a continuously updated list of the most
frequently requested URLs::

  varnishtop -i ReqURL

The following example displays a continuously updated list of the most
commonly used user agents::

  varnishtop -C -I ReqHeader:User-Agent

SEE ALSO
========

* varnishd(1)
* varnishhist(1)
* varnishlog(1)
* varnishncsa(1)
* varnishstat(1)

HISTORY
=======

The varnishtop utility was originally developed by Poul-Henning Kamp
in cooperation with Verdens Gang AS and Varnish Software AS, and later
substantially rewritten by Dag-Erling Smørgrav.  This manual page was
written by Dag-Erling Smørgrav.

COPYRIGHT
=========

This document is licensed under the same licence as Varnish
itself. See LICENCE for details.

* Copyright (c) 2006 Verdens Gang AS
* Copyright (c) 2006-2014 Varnish Software AS
