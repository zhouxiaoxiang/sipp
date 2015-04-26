Installing SIPp
================================

On Linux, SIPp is provided in the form of source code. You will need to compile SIPp to actually use it.
Pre-requisites to compile SIPp are :

-    C++ Compiler (e.g. G++ or Clang)
-    GNU Autotools (including the autotools-archive package)
-    curses or ncurses library
-    For TLS support: OpenSSL >= 0.9.8
-    For pcap play support: libpcap and libnet
-    For SCTP support: lksctp-tools
-    For distributed pauses: Gnu Scientific Libraries

You have four options to compile SIPp:

Without TLS (Transport Layer Security), SCTP or PCAP support: - This is the recommended setup if you don't need to handle SCTP, TLS or PCAP.

::

    tar -xvzf sipp-xxx.tar
    cd sipp
    autoreconf -vifs
    ./configure [--with-openssl] [--with-pcap] [--with-sctp]
    make
                

With TLS support, you must have installed OpenSSL library (>=0.9.8) (which may come with your system).
With PCAP play support:
With SCTP support:

To compile SIPp on Windows with pcap (media support), you must:

    Copy the WinPcap developer package to "C:\cygwin\lib\WpdPack"
    Remove or rename "pthread.h" in "C:\cygwin\lib\WpdPack\Include", as it interfers with pthread.h from cygwin
    Compile according to the instructions above.

