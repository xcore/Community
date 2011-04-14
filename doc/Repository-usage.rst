Repository usage
================

Cloning a repository
--------------------

The first thing you will need to do is clone the repositories you want
to use. There are a couple of things to remember.

 #. It is best to clone everything you want to use together in the same working directory.
 #. You are likely to need the `xcommon repository <https://github.com/xcore/xcommon>`_ cloned to build any software repository (see below for more details)

From the command line
.....................

From the command line you need to have git installed on your system
and then you can follow the `github instructions on forking and cloning repositories <http://help.github.com/forking/>`_.

Using the XDE
.............

If you are using the XMOS Development Tools version 11.2.0 or
later. You can install `Egit <http://www.eclipse.org/egit/>`_ into the
XDE. This add-on to eclipse integrates git functionality into the XDE.

To install Egit go to Help \> Install New Software... from within the
XDE. Then click on Add... to add a new software and add the egit
download site from the eclipse market place (at the time of writing 
this was http://download.eclipse.org/egit/updates-0.11). Then select
this site and install the Egit and Jgit add-ons.

Once you have installed the software you can configure where it places
cloned git repositories by going to Window \> Preferences \> Team \> Git
and setting the Default Repository folder.

You can now import into your workspace straight from github. If you
wish to make changes
to a repository then you will want to fork it first (see the Github
instructions on this). After this, Go to File \> 
Import \> Git \> Import Projects from Git.  Click on Clone and add the
github repository URI where indicated. You can then click on Next to
clone off github and then import any projects from within the
repository. The standard setup is to have one XDE project
for each repository.

If you are using the 10.4.2 version of the XDE or older, see :doc:`xde_104`.

The generic repository structure
--------------------------------

The vast majority of software repositories will have the same
structure and will consist of several subdirectories containing code,
documentation, auxilliary tools etc. The actual code will be split
into modules and apps.

apps and modules
................

modules
~~~~~~~

Module directories (prefixed with module\_) 
contain a set of source files that can be used in building an
application. They also contain a file called module_build_info which
contains information on how to build the files in the module and how
the module affects the build of the application.

apps
~~~~

App directories (prefixed with app\_) contain a set of source files that 
build into a single executable (.xe file). This executable is made by
compiling the application's source files and the source files from any
modules it uses. 

The modules that an application uses, along with other settings such
as compiler flags etc. are specified in a Makefile with the app_*
directory. This Makefile will include the common Makefile from the
xcommon repository which takes care of dependencies, including the
source from other modules etc.

Note that the source files in the modules is compiled separately for
each app.

Every repositories whose main purpose is to provide modules are likely
to have some apps to demonstrate/test the functionality of the
provided modules.

The xcommon repository
----------------------

The `xcommon repository <https://github.com/xcore/xcommon>`_ contains the
common infrastructure to build projects. To use it you just need to
clone it into the same working directory as the other repositories you
are using.

Building apps
-------------

Each repository has a Makefile in its top level directory. This
Makefile has targets to build all the apps within the repository. So::

     xmake all
     
will build every application. To build an individual application you
can do::

     xmake [app_name].all
     
For example in the sc_uart repository::

     xmake app_uart_test.all
     
will just build uart_test app, alternative you can do::

     cd app_uart_test
     xmake all
     
From the XDE you can add specific Make targets to a projects by
Right-clicking on a project and going to Make Targets \> Create. You can then build these
by Right-clicking on a project and going to Make Targets \> Build. To change the default target (i.e. the
target that is built when you press the build button) you need to change the Build and Clean settings found
by Right-clicking on a project and going to Properties \> C/XC Build  and clicking on the Behaviour tab.
 
Building modules
----------------

Modules do not build on their own. They have to be used by an application.

Creating new applications
-------------------------

To create a new application you need to create a new directory
containing your apps and modules in the same directory as you have
cloned all the other repos you are going to use. The best method is
to set it up as if it were an XMOS open source repository on
github. This gives you the option of creating the github repository
later (though even if you never plan to do this it is best to set it
up this way so everything plays together).

Creating a new repository structure
-----------------------------------

To create a new repository you need to clone the repository
`xcore_template <https://github.com/xcore/xcore_template>`_ and follow the instructions in the template howto.
Once you have done this you can import this new project into the XDE by doing Import \> Git (using EGit and 11.2 tools)
or Import \> General \> Existing Projects into Workspace (using the 10.4.2 tools).

Using other modules in your new application
-------------------------------------------

Once you have created a repository structure with an app subdir you
can use any of the modules within the other repositories you have
cloned by adding the module name to the USED_MODULES list in the 
application Makefile.  

.. toctree::
  :hidden:
  
  xde_104
