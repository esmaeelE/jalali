# How to create debian package


## build

`dpkg-buildpackage -b -uc -us`

https://linuxconfig.org/easy-way-to-create-a-debian-package-and-local-package-repository

http://www.nongnu.org/jcal/


why they add jdate to this file? Why not create new .install file for it?

    $ cat jcal.install 
    usr/bin/jcal
    usr/share/man/man1/jcal.1
    usr/bin/jdate
    usr/share/man/man1/jdate.1

latest package jdate need newer version of glibc

    $ ldd ./jdate 
    ./jdate: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.33' not found (required by ./jdate)
        linux-vdso.so.1 (0x00007ffc4adf9000)
        libjalali.so.0 => /lib/libjalali.so.0 (0x00007fdc932e5000)
        libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007fdc93120000)
        /lib64/ld-linux-x86-64.so.2 (0x00007fdc93515000)
