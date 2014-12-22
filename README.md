libargp
=======

*libargp* is a portable library providing the **command-line parsing functionality** of the [*argp*][GNU argp] module of the [GNU C Library][GNU libc] (*glibc*).

The source code directly utilitises the [source][GNU libc source] of glibc 2.20.

Building
--------

To build the library, simply run `./build` from the root directory of the project. This produces all output in the `output` subdirectory.

Installing
----------

To install the library, first build it, then run `./install` as superuser from the root directory of the project. This will install the library under the default prefix directory `/usr/local`.

A custom prefix directory can be specified by setting the `INSTALL_PREFIX` environment variable before installing.

Usage
-----

The API is documented in the [online manual][GNU argp] for the GNU C Library.

Updating Source Code
--------------------

An imported version of the source code for the argp module of glibc is contained within the project directory. If you wish to update this imported version to the latest source for argp, you first need to obtain a copy of [Gnulib][GNU Gnulib]. This package contains the source for GNU code (including the argp module of glibc), along with the program [`gnulib-tool`][GNU gnulib-tool], which can import such GNU code into a separate project.

To update the imported source code, first ensure that the `gnulib-tool` program of *Gnulib* (or a symbolic link pointing to it) can be found via `PATH` environment variable. Then simply run `./update-source` from the root directory of the project. You will be notified whether the update succeeds or fails; if it fails then the previous imported source will remain intact.

[GNU libc]: http://www.gnu.org/software/libc/
[GNU libc source]: https://www.gnu.org/software/libc/download.html
[GNU argp]: http://www.gnu.org/software/libc/manual/html_node/Argp.html

[GNU Gnulib]: https://www.gnu.org/software/gnulib/
[GNU gnulib-tool]: https://www.gnu.org/software/gnulib/manual/html_node/Invoking-gnulib_002dtool.html
