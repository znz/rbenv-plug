# rbenv-plug

rbenv-plug is an [rbenv](https://github.com/sstephenson/rbenv) plugin that
provides `rbenv plug` and `rbenv unplug` command to install and uninstall
rbenv plugins.

## Usage examples

To install plugins listed in [plugins](https://github.com/sstephenson/rbenv/wiki/Plugins):

    rbenv plug <plugin-name>

Install [ruby-build](https://github.com/sstephenson/ruby-build):

    rbenv plug ruby-build

Install [rbenv-update](https://github.com/rkh/rbenv-update):

    rbenv plug rbenv-update

or omit `rbenv-`:

    rbenv plug update

Install any plugins from git repository:

    rbenv plug https://github.com/sstephenson/ruby-build.git

Uninstall `rbenv-update`:

    rbenv unplug rbenv-update

or omit `rbenv-`:

    rbenv unplug update

## Installation

Simply clone the repository into the plugins directory:

    mkdir -p ~/.rbenv/plugins
    git clone https://github.com/znz/rbenv-plug.git ~/.rbenv/plugins/rbenv-plug
