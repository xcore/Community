Software Components Background
..............................

A key aim of this project is to encourage development of firmware for use in applications based on XMOS technology, and more specifically, for the development of inter operable and re-usable software. For this vision to be realised, there need to be some standards, especially for component level software.

There is value in components using a common structure, interface, test
harness, documentation, etc. This common part is still; in its infancy,
and hence the guidelines below will evolve over time.

As a standard, we suggest that all documentation is supplied in ReStructuredText format (.rst). There is a good `primer <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_ and `quick reference <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_ on sourceforge. The xdoc repository (http://github.com/xcore/xdoc) provides a useful structure for building larger reference documentation based on Sphinx, which uses ReStructuredText as its markup format (http://sphinx.pocoo.org/) .

Component Metadata
------------------

This is an abstract machine readable description of the component. This data is kept in its own file at the top level of the repo. It includes:

* A guide to expected resource usage of the component in terms of MIPs, threads, memory, ports, timers, clock blocks, synchronizers and locks. The resource usage may include some padding to ensure that future enhancements or bug fixes remain within the resource budget allocated for a component.
* A Pretty Picture. Ideally components will have a block diagram or other useful picture in SVG format with a standard filename at the top level of the repo. This is ideally incorporated in the README.rst (and hence it would appear on the repo home page). It can also be reused in the User Guide.
* API type designations (e.g. channels, shared memory etc) and component sub-category designations

README.rst
----------

A README.rst file should be placed at the top level of the repo, and github will then render it as the home page of the repo. An example can be found in the `xcore_template <https://github.com/xcore/xcore_template>`_ repo.

CHANGELOG.rst
-------------

A note in ReStructuredText format defining the changes to the component since its last release.

User Guide
----------

Ideally a component will have a User Guide covering the API, System Architecture and Key features.

Developer Documentation: Formal Spec and Testplan
-------------------------------------------------

This is an optional set of documentation. XMOS uses this internally to formally specify component and application features, which can be extracted by automated tools and associated with a formal testplan which relates testcases to features and provides a structured way of tracking the subsequent verification process. 

Developer documentation is, as you would expect, a guide for developers as opposed to end users, which is why we keep them separate. This is entirely optional, especially for simple components.

Build Infrastructure
--------------------

A key requirement for any component worthy of the term is that it has a common system for building it. An application (and more specifically, the application build infrastructure) is much more easily constructed from a series of components which already follow a similar recipe. If you clone `xcore_template <https://github.com/xcore/xcore_template>`_ then it is easy to use the makefiles from `xcommon <https://github.com/xcore/xcommon>`_ for your repo.

Test Infrastructure
-------------------

If a component has a test infrastructure, it should follow the standard test infrastructure methodology that covers the mechanism for defining unit tests using the XMOS simulator and plugin testbenches, and make it easy for developers to add new tests.

Hardware Demo/Test applications
-------------------------------

A description of a test application provided with the component in order to demonstrate or test its capability. If possible, the test application should run on a readily available development board. We believe that successful sharing of components is going to greatly improved by having components that run on common, openly specified and above all cheap development platforms to prove that they really do work! This is why we are trying to establish an `open source hardware standard <https://github.com/xcore/hw_slicekit_system>`_ project.

