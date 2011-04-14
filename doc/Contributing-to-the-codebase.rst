Contributing to the codebase
============================

When you’re ready to take the plunge, one of the most helpful ways to contribute to the Xcore open source projects is to actually submit source code. Here’s a step-by-step listing of the things you need to do to make this a successful experience. 

Learn the Language and the Framework
------------------------------------

Learn at least something about XMOS technology, XC and the Xcore open source projects - there are some pointers in :doc:`About-XMOS-technology`. Guidelines and examples of each class of open source repository can also be found in :doc:`Classes-of-Repository`.

Install git
-----------
 
The Xcore open source project uses git for source code control. The
`git homepage <http://git-scm.com/>`_ has installation instructions. If
you’re on OS X, use the `Git for OS X installer <http://code.google.com/p/git-osx-installer/>`_. If you’re unfamiliar with git, there are a variety of resources on the net that will help you learn more:

*	`Everyday Git <http://www.kernel.org/pub/software/scm/git/docs/everyday.html>`_ will teach you just enough about git to get by.
*	The `PeepCode screencast <https://peepcode.com/products/git>`_ on git ($9) is easier to follow.
*	GitHub offers links to a variety of git resources.
*	`Pro Git <http://progit.org/book/>`_ is an entire book about git with a Creative Commons license.

Pick a repository and Fork the Source Code
------------------------------------------

Unlike many open source projects, the Xcore open source project
consist of many repositories of multiple types.  We use the
Fork-And-Pull model - once you have found one that you are interested
in contributing to, you need to `create a fork <http://help.github.com/forking/>`_.

Write Your Code
---------------

Now get busy and add your code to the project (or edit the existing code). You’re on your fork now, so you can write whatever you want. But if you’re planning to submit your change back for inclusion in the Xcore open source projects, keep a few things in mind:

*	Get the code right
*	Follow community best practice
*	Include tests that fail without your code, and pass with it
*	Update the documentation

Follow the Coding Conventions
-----------------------------
 
Each repository can be expected to have its own conventions, at least initially. Please be consistent with the conventions already established in any given project. In time, the community may develop more general and more widely applicable guidelines.

Use the community licenses
--------------------------

First - you need to have filled out and clicked through the
`contributor license agreement <https://www.xcore.com/OpenSourceAgreement>`_.  This protects the community from bogus contributions and ensures that code is safe and easy for everyone to reuse.  If you've already done this and your latest contribution conforms to the requirements, you can skip this step.

Use (or at least link to) the licenses - there is one for `hardware
<https://github.com/xcore/Community/raw/gh-pages/HardwareLicense.txt>`_
and one for `software <https://github.com/xcore/Community/raw/gh-pages/SoftwareLicense.txt>`_.  Don't forget to change the copyright to your name or organisation.

For example, if you don't want to copy the license into the top of your source code, here's a lightweight alternative::

     // Copyright (c) 2011, <insert copyright holder here>, All rights reserved
     // This software is freely distributable under a derivative of the
     // University of Illinois/NCSA Open Source License posted in
     // LICENSE.txt and at <http://github.xcore.com/>

In this case you should also place the appropriate license in a LICENSE.txt file at the root of your repository.

Pull Request
------------
When you’re happy with the code on your computer, you need to do a
`pull request <http://help.github.com/pull-requests/>`_.  This (politely!) asks the maintainer to pull your changes in your fork, into the origin repository.

Iterate as Necessary
--------------------

It’s entirely possible that the feedback you get will suggest
changes. Don’t get discouraged: the whole point of contributing to an
active open source project is to tap into community knowledge. If
people are encouraging you to tweak your code, then it’s worth making
the tweaks and resubmitting. 
