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

## How to work

When `rbenv plug <git-url>`, install the plugin like installation above.

When `rbenv plug <plugin-name>`, run script in `share/rbenv-plug`.

Because most of plugins named `rbenv-*`,
arguments of `rbenv plug` and `rbenv unplug` can omit `rbenv-`.

Scripts in `share/rbenv-plug`,
`rbenv-aliases` runs `rbenv aliases` after installation,
`rbenv-use` also installs `rbenv-whatis` that required from `rbenv-use`.
