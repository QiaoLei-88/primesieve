Hacking on primesieve
=====================

### Where the source code lives

* The sieve of Eratosthenes implementation lives in [src/primesieve](src/primesieve)
* The sieve of Eratosthenes header files live in [include/primesieve](include/primesieve)
* The primesieve console application lives in [src/apps/console](src/apps/console)
* The primesieve GUI application (uses Qt) lives in [src/apps/gui](src/apps/gui)

### Understanding the source code

* Read _**Algorithms**_ and _**Implementation**_ sections from [http://primesieve.org](http://primesieve.org)
* Then read [src/primesieve/README](src/primesieve/README)

### Adding a new source file

* Add new cpp file to [src/primesieve](src/primesieve)
* Add its header file to [include/primesieve](include/primesieve)
* Add source and header files to [Makefile.am](Makefile.am) and [Makefile.msvc](Makefile.msvc)

### Versioning

* Increase version number in [include/primesieve.hpp](include/primesieve.hpp)
* Increase version number in [include/primesieve.h](include/primesieve.h)
* Increase version number in [configure.ac](configure.ac) in ```AC_INIT```
* [Increase Libtool version](http://www.gnu.org/software/libtool/manual/html_node/Updating-version-info.html) number in [configure.ac](configure.ac) in ```AC_SUBST```
* Update current year in [src/apps/console/help.cpp](src/apps/console/help.cpp)
* Update current year in [src/apps/gui/src/PrimeSieveGUI_const.hpp](src/apps/gui/src/PrimeSieveGUI_const.hpp)

### Release process

* Increase version number (see <a href="#versioning">Versioning</a>)
* Build statically linked primesieve binaries and upload them to [https://bintray.com](https://bintray.com)
* Update [ChangeLog](ChangeLog)
* Tag the new release in git
* Create a new release tarball using ```make dist``` and upload it to [https://bintray.com](https://bintray.com)