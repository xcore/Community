Hardware Designs
================

Open Hardware is an important component of open firmware, especially for a widely applicable horizontal technology like XMOS processors.

Hardware repos are the place to park your schematics, gerbers, pinout definitions and so on. Project repos can then refer to both component, application and hardware repos to pull it all together. Its quite possible that some users might love your board design but have little interest in the firmware originally written for it, so it makes sense to separate these aspects of projects.

There will be two main kinds of hw\_ repo:

   * A hardware design that is designed for use with the 
     `XCore Open Source Hardware Platform <https://github.com/xcore/hw_slicekit_system>`_.
   * Other hardware designs

The former can be considered the hardware equivalent of a compliant Software Component, in that standards for interoperability and documentation will apply. The latter is completely freestyle.

