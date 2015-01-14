# ivm

This repository began as a GitHub fork of [tj/n](https://github.com/tj/n).
Simple flavour of node binary management, no subshells, no profile setup, no convoluted api, just _simple_.

 ![](https://i.cloudup.com/59cA8VEDae.gif)

## Installation

    $ npm install -g ivm

or

    $ make install
    
to `$HOME`. Prefix later calls to `ivm` with `N_PREFIX=$HOME`

    $ PREFIX=$HOME make install

### Installing Binaries

Install a few nodes:

    $ ivm 0.8.14
    $ ivm 0.8.17
    $ ivm 0.9.6

Type `ivm` to prompt selection of an installed node. Use the up /
down arrow to navigate, and press enter or the right arrow to
select, or ^C to cancel:

    $ ivm

      1.0.0
    ο 1.0.1
      1.1.1

Use or install the latest official release:

    $ ivm latest

Use or install the stable official release:

    $ ivm stable

Switch to the previous version you were using:

    $ ivm prev

### Removing Binaries

Remove some versions:

    $ ivm rm 1.0.0 v1.0.1

Instead of using `rm` we can simply use `-`:

    $ n - 1.0.0

### Binary Usage

When running multiple versions of node, we can target
them directly by asking `n` for the binary path:

    $ n bin 1.0.0
    /usr/local/n/versions/1.0.0/bin/iojs

Or by using a specific version through `n`'s `use` sub-command:

    $ n use 1.0.0 some.js

with flags:

    $ n as 1.0.0 --debug some.js

## Usage

 Output from `ivm --help`:

    Usage: ivm [options] [COMMAND] [args]

    Commands:

      ivm                            Output versions installed
      ivm latest                     Install or activate the latest node release
      ivm stable                     Install or activate the latest stable node release
      ivm <version>                  Install node <version>
      ivm use <version> [args ...]   Execute node <version> with [args ...]
      ivm bin <version>              Output bin path for <version>
      ivm rm <version ...>           Remove the given version(s)
      ivm --latest                   Output the latest node version available
      ivm --stable                   Output the latest stable node version available
      ivm ls                         Output the versions of node available

    Options:

      -V, --version   Output current version of n
      -h, --help      Display help information

    Aliases:

      which   bin
      use     as
      list    ls
      -       rm

## Details

 `ivm` by default installs node to _/usr/local/n/versions_, from
 which it can see what you have currently installed, and activate previously installed versions of node when `ivm <version>` is invoked again.

 Activated nodes are then installed to the prefix _/usr/local_, which of course may be altered via the __N_PREFIX__ environment variable.

 To alter where `ivm` operates simply export __N_PREFIX__ to whatever you prefer.

## License

(The MIT License)

Copyright (c) 2014 TJ Holowaychuk &lt;tj@vision-media.ca&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
