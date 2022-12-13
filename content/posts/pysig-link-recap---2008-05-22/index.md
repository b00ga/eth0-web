---
title: 'PySIG Link Recap - 2008-05-22'
author: b00ga
date: 2008-05-22T18:50:28-07:00
publishdate: 2008-05-22T18:50:28-07:00
lastmod: 2013-04-10T10:07:57-07:00
draft: false
description: 'PySIG Link Recap - 2008-05-22'
categories: ['Python', 'Basic posts']
tags: ['regular']
---

Arrived later than usual, traffic on Rt. 3 was extra retarded. Start planning for [Software Freedom Day](http://softwarefreedomday.org/) activities. This year it's on September 20, 2008. Kent asked about accessing existing C++ code from Python. Arc recommended [Boost](http://www.boost.org/users/) or possibly [SWIG](http://www.swig.org/). Shawn mentioned that if you need to access C libraries, that [ctypes](http://python.net/crew/theller/ctypes/) may be useful, but Arc said there can be some caveats to how well it can work. This led into discussions of other projects for doing things like writing Python modules with packages that will build out to C. The two main projects in this space that came up were [cython](http://cython.org/) and [Pyrex](http://www.cosc.canterbury.ac.nz/greg.ewing/python/Pyrex/). A [recent discussion](http://dlslug.org/pipermail/python-talk/2008-May/000776.html) on python-talk about interacting with Excel from Python was rehashed in person. A copy of [O'Reilly's](http://www.ora.com/) [Python Programming On Win32](http://www.oreilly.com/catalog/9781565926219/index.html) found it's way to the meeting, and is a good starting point for attacking this problem. Ted has been having headaches with Unicode text files (and receiving text possibly in other encodings). Kent suggested [Universal Encoding Detector](http://chardet.feedparser.org/) to help with the problem. Announcement from Ray: His company, [Appropriate Solutions](http://www.appropriatesolutions.com/), is now a silver sponsor of [Twisted](http://twistedmatrix.com/). [Kent's Korner](http://personalpages.tds.net/~kent37/kk/): This month's [Kent's Korner presentation](http://personalpages.tds.net/~kent37/kk/00011.html) shows us the enhanced python shell [IPython](http://ipython.scipy.org/). Flip through the [User Manual](http://ipython.scipy.org/doc/manual/index.html) to dive in. -Shawn
