Classes of Repositories
=======================

Unlike many open source projects, the Xcore  open source project consists of many different classes of design, and we expect the number of classes may also grow over time.  Each class may have its own conventions - for example, creating a v1 release of a software component will have a completely different set of requirements to the release of a v1 printed circuit board.  There may be other differences relating to how a project is built and tested etc.

The following lists the different classes that we currently use and/or expect in the future.  The links are to pages which describe attributes that they share in common, which could relate to build systems, test infrastructure, versioning etc.  These restrictions enable the use of automated build and regression systems, which we can all use to interpret the status and maturity of development projects:

* :doc:`Software-components` are bits of code that can be used in applications. They are written for other developers, and can be integrated by other developers. Software components may require a specific peripheral device on one or more I/O ports.
* :doc:`Applications` are programs that are designed for an end-user. An application may use code form one or more Software components. Applications are often written for a particular hardware platform that incorporates specific peripheral devices on specific I/O pins.
* :doc:`Hardware-designs` are schematics and or gerber files that specify a design that incorporates one or more XCores. Hardware designs often have a port-map stating which device is connected to which I/O port, and a network description. 
* :doc:`Tools` are programs that are used by developers to create software and/or hardware. Example tools are assemblers, debuggers, and compilers. Some tools will not be hosted in github, because they have a home elsewhere (for example, the LLVM compiler).

Follow the links above to find out more, or, to contribute your views in how the community should manage this diversity, post to the `Xcore open source project user forum`_

.. _Xcore open source project user forum: https://www.xcore.com/forum/viewforum.php?f=32

.. toctree::
   :hidden:

   Software-components
   Applications
   Hardware-designs
   Tools
