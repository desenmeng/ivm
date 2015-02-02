# [nvm](https://github.com/creationix/nvm) has supported io.js, nvm is a better choice to manage multiple active node.js&io.js versions

# ivm

This repository began as a GitHub fork of [tj/n](https://github.com/tj/n).
Simple flavour of node binary management, no subshells, no profile setup, no convoluted api, just _simple_.


## Installation

    $ npm install -g ivm



## Help

    $ ivm --help

## Useage
Useage go straight to [n](https://github.com/tj/n)

**Just change n to ivm**

![](https://i.cloudup.com/59cA8VEDae.gif)

![snip20150114_35](https://cloud.githubusercontent.com/assets/1209159/5735628/e3b2e7ba-9c03-11e4-91df-e346a307a70d.png)



### Installing Binaries

Install iojs:

    $ ivm 1.0.0
    $ ivm 1.0.1

Type `ivm` to prompt selection of an installed node. Use the up /
down arrow to navigate, and press enter or the right arrow to
select, or ^C to cancel:

    $ ivm

      1.0.0
    ο 1.0.1

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
them directly by asking `ivm` for the binary path:

    $ ivm bin 1.0.0
    /usr/local/iojs/versions/1.0.0/bin/iojs

Or by using a specific version through `ivm`'s `use` sub-command:

    $ ivm use 1.0.0 some.js

with flags:

    $ ivm as 1.0.0 --debug some.js








