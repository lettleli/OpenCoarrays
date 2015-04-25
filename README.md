# OpenCoarrays #

## Overview ##
This archive contains the [OpenCoarrays](http://www.opencoarrays.org) source code, tests, and documentation. OpenCoarrays is an open-source software project for developing, porting and tuning transport layers that support coarray Fortran compilers.  We target compilers that conform to the coarray parallel programming features in Fortran 2008. We also support several features proposed for Fortran 2015 in the draft Technical Specification [TS18508 Additional Parallel Features in Fortran](http://isotc.iso.org/livelink/livelink?func=ll&objId=16769292&objAction=Open).

Coarray Fortran enables application developers to express parallel algorithms without hardwiring a particular version of a particular communication library into their codes.  Such abstraction makes application code less sensitive to the evolution of the underlying communication libraries and hardware platforms.

OpenCoarrays offers similar investment-protection to compiler developers.  Compilers make high-level communication and synchronization requests through OpenCoarrays, which translates the requests into lower-level calls to a user-specified communication library.  A user of an OpenCoarrays-compatible compiler can link compiler-generated object files to the communication library deemed most appropriate and efficient for the target application and platform.  Currently supported communication libraries include the Message Passing Interface ([MPI](http://www.mpi-forum.org)) and the Global Address Space Network ([GASNet](http://gasnet.lbl.gov)).

## Compatible Compilers ##
Since version 5.0.0, the GNU Fortran ([GFortran](https://gcc.gnu.org/wiki/GFortranBinaries)) compiler, which is part of the GNU Compiler Collection ([GCC 5](https://gcc.gnu.org/)), is OpenCoarrays-compatible.  If you would like to use OpenCoarrays with a different compiler, please let the compiler vendor and the OpenCoarrays project team know.

## Prerequisites ##
We expect our LIBCAF_MPI library to be the default on systems that have MPI 3.0.  LIBCAF_MPI is the most straightforward to install and use and the most robust in terms of its internal complexity.  LIBCAF_MPI currently supports the use of the [MPICH](http://www.mpich.org) implementation of MPI.  We also recommend to use [MVAPICH](http://mvapich.cse.ohio-state.edu/) when possible in order to get higher performance.

We also offer a LIBCAF_GASNet that builds atop the Global Address Space Networking ([GASNet](http://gasnet.lbl.gov)) communication library.  We intend for LIBCAF_GASNet to be an ``expert'' alternative capable of outperforming MPI for some applications on some platforms.  LIBCAF_GASNet requires greater care to configure and use.


## Installation ##

Please see the INSTALL file.

## Documentation ##

To generate automated documentation, install [Robodoc](http://rfsber.home.xs4all.nl/Robo/) and execute the command "robodoc" at the command line inside the "doc" subdirectory.  Then open the resulting doc/html/toc_index.html file with a web browser.

## Contributing ##

Please see the CONTRIBUTING file.

## Support ##

* We respond to support questions via the [OpenCoarrays Google Group](https://groups.google.com/forum/#!forum/opencoarrays); to subscribe, log-in with your Google account or [subscribe](https://groups.google.com/forum/#!forum/opencoarrays/join) with any email address.
* We offer an additional [menu](http://opencoarrays.org/services) of services on a contract basis.

## Acknowledgements ##
We gratefully acknowledge support from the following institutions:

* [National Center for Atmospheric Research](http://ncar.ucar.edu) for access to the Yellowstone/Caldera supercomputers and for logistics support during the initial development of OpenCoarrays.
* [CINECA](http://www.cineca.it/en) for access to Eurora/PLX for the project HyPS- BLAS under the ISCRA grant program for 2014.
* [Google](http://google.com) for support of a related [Google Summer of Code](https://www.google-melange.com) 2014 project.
* The National Energy Research Scientific Computing Center ([NERSC](http://www.nersc.gov)), which is supported by the Office of Science of the U.S. Department of Energy under Contract No. DE-AC02-05CH11231, for access to the Hopper and Edison supercomputers under the OpenCoarrays project start allocation.
* [Sourcery, Inc.](http://www.sourceryinstitute.org), for financial support for the domain registration, web hosting, advanced development, and conference travel.
