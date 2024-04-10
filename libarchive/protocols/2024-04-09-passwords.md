# Protocol

## Summary

- Attendees: 1
- Duration: 3 h

Try debugger in Visual Studio Code with bsdtar. Start reading code
by following debugger. Switched to unit tests for debugging.

# Timeline

Due to my lack of in-depth knowledge of Visual Studio Code and Windows
debugging, I was unable to easily set up bsdtar.exe in a way to debug
archive creation.

Fortunately a lot of unit tests exist, which can be easily debugged
through CMake support.

Started inspecting bsdtar's main function and following its path.

At some point, I went down the passphrase rabbit hole. While being in
there, I discovered that Windows' readpassphrase allows empty input
which erroneously stays `\r\n` without stripping these characters.

Wrote a patch and submitted a PR to libarchive:
- https://github.com/libarchive/libarchive/pull/2115

Empty passwords are generally not allowed for archive encryption, but
actually it is possible to circumvent this check.

Wrote a patch and submitted a PR to libarchive:
- https://github.com/libarchive/libarchive/pull/2116
