VDR UPnP Server
===============

The purpose of this program is to serve VDR Recordings (only TS format for now)
via UPnP across a network.

It is deliberately NOT a VDR plugin and is supposed to be run on a
simple/low-energy file server, allowing the VDR computer to be turned
off or in standby when it is not recording.

Why a dedicated server?
-----------------------

VDR has a unique file format, using plain MPEG-TS files as recording, and
embedding metadata in directory names (date/time/channel number), a binary
index file for frame-exact seeking and a plain-text info file for information
such as framerate and EPG.

Because the format is so application-specific it does not make much sense to
integrate this into general-purpose UPnP-Servers, and since most devices
have hardware decoders for the standard television formats no transcoding
(which many UPnP servers do) is necessary.
