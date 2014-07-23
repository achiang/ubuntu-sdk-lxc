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

Usage
=====

  - Run the ``create`` script with sudo privileges.
  - Use the ``build`` script to compile your project inside the container.
    You will need to modify it appropriately, and this is still part of
    the WIP nature of these tools
  - Use the ``run`` script to run your project inside the container. The
    GUI component should automatically appear on your host desktop. This
    script will need modification for your project as well.

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
