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
