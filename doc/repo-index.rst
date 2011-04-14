Repository index
================

Below is a list of repositories, roughly classified by purpose. Some
repositories are in a class of their own and are, until other similar
repositories appear, held in a *miscellaneous* category. These categories
are necessarily crude, and will hopefully improve over time.

- Software components and applications that execute on an XCore:

  - I/O:

    - `Serial interfaces`_ such as SPI, UART, JTAG, ...

    - `Analogue interfaces`_ such as PWM

  - `Networking`_ such as USB, Ethernet

  - `Numerical`_ fixed point, DSP, filters, transforms

  - `Unclassified applications`_ Miscellaneous applications.

- `Boards`_ standard software on boards.

- `Tools`_ compilers, debuggers, probing

- `Documents`_ 

- `Infrastructure`_ needed for any or some of the above.


I/O interfaces
--------------

Serial interfaces
.................

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`sc_jtag </xcore/sc_jtag>`_                                     JTAG communication protocols
`sc_spdif </xcore/sc_spdif>`_                                   S/PDIF TX and RX component
`sc_spi </xcore/sc_spi>`_                                       SPI Master/Slave Software Component
`sc_uart </xcore/sc_uart>`_                                     UART Components
`sc_fram_if </xcore/sc_fram_if>`_                               A lightweight SPI F-RAM interface.
=============================================================== =========================================================================================================

Analogue interfaces
...................

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`sc_class_d_amplifier </xcore/sc_class_d_amplifier>`_           Class D amplifier
`sc_pwm </xcore/sc_pwm>`_                                       Pulse Width Modulation (PWM) components
`sc_capacitive_sensing </xcore/sc_capacitive_sensing>`_         Capacitive sensing (capsens) on an XCore
=============================================================== =========================================================================================================

Networking
----------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`sc_usb </xcore/sc_usb>`_                                       USB device library
`sc_ethernet </xcore/sc_ethernet>`_                             10/100 Mii ethernet mac and filters
`sc_xtcp </xcore/sc_xtcp>`_                                     micro TCP/IP stack for use with sc_ethernet
=============================================================== =========================================================================================================

Numerical
---------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`ap_par_audio_dsp </xcore/ap_par_audio_dsp>`_                   Parallel Audio DSP example
`sc_dsp_filters </xcore/sc_dsp_filters>`_                       Standard DSP filters, such as Biquads and FIRs
`sc_dsp_transforms </xcore/sc_dsp_transforms>`_                 DSP transforms, such as DCT.
`sc_lib_fixed_point </xcore/sc_lib_fixed_point>`_               A fixed point library with functions that manipulate 8.24 fixed point numbers.
=============================================================== =========================================================================================================

Unclassified applications
-------------------------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`ap_led_tile_controller </xcore/ap_led_tile_controller>`_       LED Tile Controller
`ap_pintest </xcore/ap_pintest>`_                               Application for testing pin connectivity
`sc_crypto </xcore/sc_crypto>`_                                 Cryptographic algorithms for the XCore
=============================================================== =========================================================================================================

Boards
------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`proj_shift_registers </xcore/proj_shift_registers>`_           Shift register board
`proj_xmp64 </xcore/proj_xmp64>`_                               Project repository for the XMP 64 multiprocessor board
`proj_xtag2 </xcore/proj_xtag2>`_                               XTAG2 hardware and software
`hw_slicekit_system </xcore/hw_slicekit_system>`_               Specifications and use models for Open Source Modular Development Hardware for XMOS applications 
=============================================================== =========================================================================================================

Tools
-----

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`tool_sire </xcore/tool_sire>`_                                 Language and runtime system for dynamic process creation
`tool_pyxsim </xcore/tool_pyxsim>`_                             Python wrapper for the XMOS simulator testbench
`sc_xlog </xcore/sc_xlog>`_                                     Logging component
`sc_lib_xscope </xcore/sc_lib_xscope>`_                         Device side xscope library
`ap_xscope_examples </xcore/ap_xscope_examples>`_               Examples on how to use the xscope tracing library
=============================================================== =========================================================================================================

Documents
---------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`doc_tips_and_tricks </xcore/doc_tips_and_tricks>`_             Various tricks on how to program an XS1
=============================================================== =========================================================================================================


Infrastructure
--------------

=============================================================== =========================================================================================================
Repository                                                      Purpose
=============================================================== =========================================================================================================
`xcommon </xcore/xcommon>`_                                     Common application framework for XMOS software
`xdoc </xcore/xdoc>`_                                           Common infrastructure for code documentation
`xcore.github.com </xcore/xcore.github.com>`_                   Community web stuff, in HTML
`Community </xcore/Community>`_                                 Community web stuff and documentation (including this file)
`sc_lib_example </xcore/sc_lib_example>`_                       This repo is an example of how to build modules that can make an exportable binary library.
`xcore_template </xcore/xcore_template>`_                       A template for a sc repository module
=============================================================== =========================================================================================================
