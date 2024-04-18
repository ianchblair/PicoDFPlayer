# PicoDFPlayer

MicroPython Driver for the DFPlayer (and clones) MP3 Player on Raspberry Pi Pico

This driver implements the serial UART communication protocol that the DFPlayer use and adds shorthand functions for the most common features for controlling the DFPlayer such as play a track, change volume, next/previous track, volume controls etc.

It is also possible to directly send commands to the DFPlayer through the driver, for instance if you want to handle the return values and/or use features that are not implemented as shorthand features.

This version is extended by Ian Blair to make acknowledgement handling and timer use optional, so that command wait timer can be managed by calling task, when using asyncio.

Begin function, with optional reset (ox0C) call and function for play (0x03) commands added.
