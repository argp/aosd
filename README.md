# Apple Open Source Downloader (aosd)

This is my fork of [samdmarshall's](https://github.com/samdmarshall]
really [helpful utility](https://github.com/samdmarshall/AOS-Downloader)
to download Apple's open source code packages.

I made some changes specific to the way I want to use it; most probably
they are not appropriate for what you want to do. Please use the
[upstream version](https://github.com/samdmarshall/AOS-Downloader)
instead.

If, despite the warning, you want to use it, be sure to change
`download_directory` in `aosd/downloader/config.py` and
`aosd/data/aosd.plist`.

Then you can do something like:

```
$ python aosd/main.py -t mac -p dyld -r 10.11.2
====================
[INFO]: Downloaded "dyld-360.18" to "/home/argp/archive/osx/kernel/10.11.2/dyld-360.18.tar.gz"
[INFO]: The package "dyld-360.18" has been downloaded to "/home/argp/archive/osx/kernel/10.11.2".
====================
```

All bugs are mine, if you use this fork don't bother samdmarshall; contact
me instead.
