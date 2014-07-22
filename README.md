ubuntu-sdk lxc wrappers
=======================

Currently, developing Ubuntu Phone apps while using Ubuntu 14.04 LTS (Trusty)
can be challenging, because many of the latest phone APIs have not been
(and will never be) backported to trusty.

Thus, the only way to build and test your app is to deploy it on a phone
or use an emulator.

These scripts provide an alternative solution:

    - host the Ubuntu SDK inside an LXC container
    - transparently export the container's $DISPLAY to your trusty desktop
    - build your app inside the container, using the latest Utopic APIs
    - run the app on your desktop for faster build/test/debug cycles

Status
======

These are definitely still a rough work-in-progress, but at least they prove
the concept.

TODO
====

    - it may be better to build the app *outside* the container and only
      *run* inside the container

Credits
=======
    - Stephane Graber
    - Scott Sweeny
