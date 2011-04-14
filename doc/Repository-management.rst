Repository management
=====================

A repository may contain several modules for use. As a general guide,
modules with very disparate functionality should not be grouped into the
same repository. The idea is to group modules that are going to be
developed, maintained and released as a set (e.g. uart_rx and uart_tx).

Adding a repository
-------------------

If you have looked around, and are satisfied that your design warrants a new repository, you will need to request that one is added.  At present new repositories can only be added by the community manager
on github, but don't worry - the community manager won't reject
reasonable requests.  To request a repository, `file an issue on the Community Repository <https://github.com/xcore/Community/issues>`_.

Before asking for a new repository you should try and create the new
structure locally and start work on the project. Follow the
instructions in :doc:`Repository-usage` to see how to do this.

As well as creating a repository, the community manager will create a team with the same name, the members of which will have push and pull rights to that repo.  This will normally just have the requestor on it in the first instance.

Naming convention
-----------------

When filing your issue requesting a new repo, please make the subject line read::

  repo request \<repo_name\>

The repo_name should begin with one of the following prefixes:

*	sc_*<name>* for a software component
*	hw_*<name>* for a hardware design
*	ap_*<name>* for a full application (comprising multiple components)
*	proj_*<name>* for a full project (comprising an application and hardware)

Of course before requesting a new repo, please first consider whether it might better belong as part of an existing repo.

Adding a committer
------------------

The maintainer can request that a committer is added to their repo by 
`filing an issue on the Community Repository <https://github.com/xcore/Community/issues>`_.  The committer will be placed in the repo Team alongside the maintainer and other committers.

Adding your repository to the automated build system
----------------------------------------------------

In time, we plan to provide an automated nightly build system.  For a successful build, your design must follow the structural guidelines defined for its repository class (see :doc:`Classes-of-Repository`).  Build status will be updated daily on the :doc:`repo-index`.

The community manager will announce when this facility is available and how to add your repository.

Adding your repository to the automated regression system
---------------------------------------------------------

In time, we plan to provide an automated nightly regression system.  For a successful regression, your design must follow the structural and test guidelines defined for its repository class (see :doc:`Classes-of-Repository`).  Regression status, which will also provide basic metrics like code coverage, will be updated daily on the :doc:`repo-index`.

The community manager will announce when this facility is available and how to add your repository.

Doing your own thing
--------------------

Note that while we plan to offer these automation facilities as a service to the community, that does not mean that they are mandatory. The intention is to allow our users to subscribe to these services (and thus have the resulting status visible for their project) on a service by service basis as and when they feel ready, or perhaps, not at all.

