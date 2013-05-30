==========
 pySerial
==========

概览
====
This module encapsulates the access for the serial port. It provides backends
for Python running on Windows, Linux, BSD (possibly any POSIX compliant
system), Jython and IronPython (.NET and Mono). The module named "serial"
automatically selects the appropriate backend.

It is released under a free software license, see LICENSE_ for more
details.

Copyright (C) 2001-2010 Chris Liechti <cliechti(at)gmx.net>

Other pages (online)

- `project page on SourceForge`_
- `SVN repository`_
- `Download Page`_ with releases
- This page, when viewed online is at http://pyserial.sf.net.

.. _LICENSE: appendix.html#license
.. _`project page on SourceForge`: http://sourceforge.net/projects/pyserial/
.. _`SVN repository`: http://sourceforge.net/svn/?group_id=46487
.. _`Download Page`: http://sourceforge.net/project/showfiles.php?group_id=46487


特性
====
- Same class based interface on all supported platforms.
- Access to the port settings through Python properties.
- Support for different byte sizes, stop bits, parity and flow control with
  RTS/CTS and/or Xon/Xoff.
- Working with or without receive timeout.
- File like API with "read" and "write" ("readline" etc. also supported).
- The files in this package are 100% pure Python.
- The port is set up for binary transmission. No NULL byte stripping, CR-LF
  translation etc. (which are many times enabled for POSIX.) This makes this
  module universally useful.
- Compatible with :mod:`io` library (Python 2.6+)
- RFC 2217 client (experimental), server provided in the examples.


要求
====
- Python 2.3或更高，包括Python 3.x
- ctypes extensions on Windows (is in standard library since Python 2.5+)
- "Java Communications" (JavaComm) or compatible extension for Java/Jython


安装
====

pyserial
--------
This installs a package that can be used from Python (``import serial``).

To install the module for all users on the system, administrator rights (root)
is required..

从源代码（tar.gz或checkout）
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
从 http://pypi.python.org/pypi/pyserial 下载压缩包。
解压，进入``pyserial-x.y``目录并运行::

    python setup.py install

对于Python 3.x::

    python3 setup.py install

从PyPI
~~~~~~
Alternatively it can be installed from PyPI, either manually downloading the
files and installing as described above or using::

    pip install pyserial

or::

    easy_install -U pyserial

Packages
~~~~~~~~
There are also packaged versions for some Linux distributions and Windows:

Debian/Ubuntu
    A package is available under the name "python-serial". Note that some
    distributions package an older version of pySerial.

Windows
    There is also a Windows installer for end users. It is located in the
    PyPi_.  Developers may be interested to get the source archive, because it
    contains examples and the readme.

.. _PyPi: http://pypi.python.org/pypi/pyserial


参考
====
* Python: http://www.python.org/
* Jython: http://www.jython.org/
* Java@IBM: http://www-106.ibm.com/developerworks/java/jdk/ (JavaComm links are
  on the download page for the respective platform JDK)
* Java@SUN: http://java.sun.com/products/
* IronPython: http://www.codeplex.com/IronPython
* setuptools: http://peak.telecommunity.com/DevCenter/setuptools


旧版本
======
Older versions are still available on the `Download Page`_. pySerial 1.21 is
compatible with Python 2.0 on Windows, Linux and several un*x like systems,
MacOSX and Jython.

On windows releases older than 2.5 will depend on pywin32_ (previously known as
win32all)

.. _`Download Page`: http://sourceforge.net/project/showfiles.php?group_id=46487
.. _pywin32: http://pypi.python.org/pypi/pywin32
