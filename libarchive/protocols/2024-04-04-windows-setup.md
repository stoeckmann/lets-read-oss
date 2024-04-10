# Protocol

## Summary

- Attendees: 2
- Duration: 3 h

Set up Windows 11 64 bit with Visual Studio Code to be able to compile
libarchive and use debugger for further analysis.

# Timeline

The libarchive project can be easily checked out from GitHub through
GitLens. Special care has to be taken when using CMake though:

By default, CMake builds with Debug profile. The Debug profile enables
-Werror, which does not properly work with Visual Studio 2022. I had
to set line 99 of CMakeLists.txt to OFF explicitly to have debug symbols
and the possibility to compile libarchive.

Alternatively, setting CMake profile to Release fixes the compilation.

Tests can be run, but some fail. Further investigation is needed.

Many generated files are shown in GitLens. The generated binaries are
located in build/bin/Debug.

No optional dependencies have been installed, which means that,
for example, xar support does not exist.

Also Linux 64 bit system has been prepared to compile and debug
libarchive. Optional dependencies are available here.
