Digibyte Core 8.21.1 staging tree
=================================

https://digibyte.io/


What is Digibyte?
-----------------

Digibyte is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Digibyte uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Digibyte Core is the name of open source
software which enables the use of this currency.

For more information, as well as an immediately usable, binary version of
the Digibyte Core software, see https://digibyte.io/, or check the source code
available from https://github.com/digibyte-core/digibyte/.


How do I build the software?
----------------------------

The example below presumes you have a basic build environment installed; shown is Debian 10 (buster), on unstable packages branch.

### Static compile

    git clone https://github.com/digibyte-core/digibyte/
    cd digibyte
    git checkout 8.21.1
    cd depends
    make HOST=x86_64-linux-gnu
    cd ..
    ./autogen.sh
    CONFIG_SITE=$PWD/depends/x86_64-linux-gnu/share/config.site ./configure
    make

License
-------

Digibyte Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

