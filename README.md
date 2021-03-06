Go
========

Ansible role that installs Go (https://golang.org/). The latest stable release that has been compiled for x86 64-bit Linux systems is installed by default, and different platforms and versions are supported by modifying the role variables.

This role also supports package installs on Debian based systems.

Role Variables
--------------

All of these variables are optional and should only be changed if you need to install a different version of Go (e.g. if you are installing on FreeBSD, or if you need to use an earlier release).

go_version: The version of golang to install.

go_install_method: Can be either `tar` or `package`.

go_install_dir: Installation directory.

go_root_bin_dir: Location of go binaries.

go_package_name: Name of package to install (when `go_install_method: package`).

go_download_location: The full download URL. This variable simply appends the go_tarball variable onto the Go Download URL. This should not need to be modified.

go_tarball: The tarball that you want to install. A list of options can be found on the [Go Downloads page](https://golang.org/dl/). The default is the official x86 64-bit Linux tarball for the latest stable release.

go_tarball_checksum: This variable specifies the algorithm and checksum for the tarball that you want to install (e.g. `sha1:c7d78ba4df574b5f9a9bb5d17505f40c4d89b81c` or `sha256:a96cce8ce43a9bf9b2a4c7d470bc7ee0cb00410da815980681c8353218dcf146`). The default is the SHA256 checksum of the official x86 64-bit tarball for the latest stable release. Checksums can be found on the [Go Download Page](https://golang.org/dl/).

License
-------

The MIT License (MIT)

Copyright (c) 2013 Joshua Lund

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
