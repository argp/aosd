# Apple Open Source Downloader (aosd)

This is my fork of [samdmarshall's](https://github.com/samdmarshall)
really [helpful utility](https://github.com/samdmarshall/AOS-Downloader)
to download Apple's open source code packages. I made some changes
specific to the way I want to use it; most probably they are not
appropriate for what you want to do. Please use the
[upstream version](https://github.com/samdmarshall/AOS-Downloader)
instead.

If, despite the warning, you want to use it, here's the help message:

```
$ python main.py -h
usage: main.py [-h] [-t TYPE] [-r RELEASE] [-o DESTDIR] [-l] [-p PACKAGE]
               [-b BUILD] [-d DIFF DIFF] [-s] [-c] [-f] [-v]

Apple Open Source Package Downloader

optional arguments:
  -h, --help            show this help message and exit
  -t TYPE, --type TYPE  specify the release type
  -r RELEASE, --release RELEASE
                        specify the OS X release number
  -o DESTDIR, --destdir DESTDIR
                        specify the destination directory
  -l, --list            list versions of a package to check out, if no package
                        is specified it lists available packages
  -p PACKAGE, --package PACKAGE
                        specify the name of a package from a release
  -b BUILD, --build BUILD
                        specify the build number from a package
  -d DIFF DIFF, --diff DIFF DIFF
                        specify the build number of a package to create diff
                        against
  -s, --resetcache      removes currently cached package plist files
  -c, --buildcache      caches the package manifests and builds an index
  -f, --findhash        gets the hash for the specified build number of a
                        package of a release type
  -v, --version         prints the version information
```

Then you can do something like:

```
$ python aosd/main.py -o /tmp -t mac -p dyld -r 10.11.2
====================
[INFO]: Downloaded "dyld-360.18" to "/tmp/10.11.2/dyld-360.18.tar.gz"
[INFO]: The package "dyld-360.18" has been downloaded to "/tmp/10.11.2".
====================
```

All bugs you encounter in this are probably mine, if you use this fork
don't bother samdmarshall with them; contact me instead.
