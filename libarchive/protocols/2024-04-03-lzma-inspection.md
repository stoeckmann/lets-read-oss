# Protocol

## Summary

- Attendees: 1
- Duration: 2 h

In this initial session I have inspected libarchive to see if it fits
into general scopes of Let's Read Open Source Software. Based on the
findings of the xz incident, I took a quick look at lzma-related code.

# Timeline

Retrieved libarchive from GitHub and searched for lzma in C code. This
was done merely to have a starting point. No indication exists that any
harmful code would be found.

Checked if xar, one format which can use lzma, is reachable from VLC or
Windows ZIP Tool. Both programs use libarchive internally. Turns out
that xar is only reachable from VLC if system libraries on Linux are
used, e.g. on Arch Linux.

Took a closer look into xar.

Decided that libarchive can be an interesting project to investigate as
a group. In fact, libarchive was suggested.
