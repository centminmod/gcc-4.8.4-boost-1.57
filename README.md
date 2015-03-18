# gcc-4.8.4-boost-1.57
====================
Bash script and Makefile to install gcc 4.8.4 and boost 1.57 on CentOS and Mac OS X.

To use it:

    $ mkdir -p /opt
    $ mkdir -p /opt/gcc484
    $ cd /opt/gcc484
    $ git clone https://github.com/centminmod/gcc-4.8.4-boost-1.57.git 4.8.4
    $ cd 4.8.4
    $ chmod 0700 bld.sh
    $ make

To clean up and remove everything you can run

    $ make clean

or

    $ make clean-all

what they specifically clean up

    clean-all:
        rm -rf bld src rtf archives logs
    
    clean:
        rm -rf bld src rtf *~


For more detailed information see http://joelinoff.com/blog/?p=1514.

Script details
====================

This script creates 4 subdirectories:

    Directory  Description
    =========  ==================================================
    archives   This is where the package archives are downloaded.
    src        This is where the package source is located.
    bld        This is where the packages are built from source.
    rtf        This is where the packages are installed.

When the build is complete you can safely remove the archives, bld and src directory trees to save disk space. In fact you can remove everything under directory /opt/gcc484/4.8.4/ except the contents of the /opt/gcc484/4.8.4/rtf directory tree to save disk space.

Packages Installed
====================

* binutils    2.24    http://ftp.gnu.org/gnu/binutils
* boost       1.57.0  http://sourceforge.net/projects/boost/files/boost
* cloog       0.18.3  http://www.bastoul.net/cloog
* gcc         4.8.4   http://ftp.gnu.org/gnu/gcc
* gmp         6.0.0a   http://gmplib.org/
* libiconv    1.14    http://ftp.gnu.org/pub/gnu/libiconv
* mpc         1.0.2   http://www.multiprecision.org/mpc
* mpfr        3.1.2   http://www.mpfr.org
* ppl         1.1     http://bugseng.com/products/ppl

