# Freeswitch deb builder

This builds the PhoneBo.cx Freeswitch debs.

# Usage

It's pretty simple. Pull the repo on a machine that has docker, and
run `make debs`. 

## ccache

To massively speed up builds (especially when working on patches),
ccache is installed into /usr/local/ccache. Make sure you have some
spare space on the machine you're building on

## Patches

Add patches to the `patches` folder. Currently only `patches/freeswitch` is
used, but the code should be simple enough to expand to other packages that
are built

# How does it all work?

There's a base image, which contains all the tools needed to build all the
packages. That base image is then extended with every deb that is built,
eventually ending up with a docker image that has all the requirements
to build the latest Freeswitch build.

It's all chained together by the Makefiles in the `includes` folder.


