
# Osmium Command Line Tool

A multipurpose command line tool for working with OpenStreetMap data based on
the Osmium library.

Official web site: http://osmcode.org/osmium-tool/

[![Build Status](https://secure.travis-ci.org/osmcode/osmium-tool.svg)](http://travis-ci.org/osmcode/osmium-tool)
[![Build Status](https://ci.appveyor.com/api/projects/status/github/osmcode/osmium-tool?svg=true)](https://ci.appveyor.com/project/Mapbox/osmium-tool)

## Prerequisites

You need a C++11 compliant compiler. GCC 4.8 and later as well as clang 3.6 and
later are known to work. It also works on modern Visual Studio C++ compilers.

You also need the following libraries:

    Libosmium (>= 2.13.1)
        http://osmcode.org/libosmium
        Debian/Ubuntu: libosmium2-dev

    Protozero (>= 1.5.1)
        https://github.com/mapbox/protozero
        Debian/Ubuntu: libprotozero-dev
        Fedora: protozero-devel

    Utfcpp
        This is included in the libosmium repository and might or might not
        have been installed with it. See the libosmium README.
        http://utfcpp.sourceforge.net/
        Debian/Ubuntu: libutfcpp-dev
        openSUSE: utfcpp
        Fedora: utf8cpp-devel

    RapidJSON (>= 1.1)
        This is included in the osmium-tool repository, so you usually do
        not need to install this.
        http://rapidjson.org/
        Debian/Ubuntu: rapidjson-dev

    boost-program-options (>= 1.55)
        http://www.boost.org/doc/libs/1_55_0/doc/html/program_options.html
        Debian/Ubuntu: libboost-program-options-dev

    boost-crc
        http://www.boost.org/doc/libs/1_55_0/libs/crc/
        Debian/Ubuntu: libboost-dev

    bz2lib
        http://www.bzip.org/
        Debian/Ubuntu: libbz2-dev
        Fedora: bzip2-devel
        CentOS: bzip2-devel

    zlib
        http://www.zlib.net/
        Debian/Ubuntu: zlib1g-dev
        openSUSE: zlib-devel
        Fedora: zlib-devel
        CentOS: zlib-devel

    Expat
        https://libexpat.github.io/
        Debian/Ubuntu: libexpat1-dev
        openSUSE: libexpat-devel
        Fedora: expat-devel
        CentOS: expat-devel

    cmake
        http://www.cmake.org/
        Debian/Ubuntu: cmake
        openSUSE: cmake
        Fedora: cmake

    Pandoc
        (Needed to build documentation, optional)
        http://johnmacfarlane.net/pandoc/
        Debian/Ubuntu: pandoc
        openSUSE: pandoc
        Fedora: pandoc


## Building

Osmium uses CMake for its builds, as follows:

    mkdir build
    cd build
    cmake ..
    make

To set the build type call cmake with `-DCMAKE_BUILD_TYPE=type`. Possible
values are empty, Debug, Release, RelWithDebInfo, MinSizeRel, and Dev. The
default is RelWithDebInfo.


## Documentation

See the [Osmium Tool website](http://osmcode.org/osmium-tool/)
and [Osmium Tool Manual](http://osmcode.org/osmium-tool/manual.html).

There are man pages in the 'man' directory. To build them you need 'pandoc'.
If the `pandoc` command was found during the CMake config step, the manpages
will be built automatically.


## Tests

Call `ctest` in the build directory to run the tests after build.

More extensive tests of the libosmium I/O system can also be run. See
`test/io/Makefile.in` for instructions.


## License

Copyright (C) 2013-2017  Jochen Topf (jochen@topf.org)

This program is available under the GNU GENERAL PUBLIC LICENSE Version 3.
See the file LICENSE.txt for the complete text of the license.


## Authors

This program was written and is maintained by Jochen Topf (jochen@topf.org).

