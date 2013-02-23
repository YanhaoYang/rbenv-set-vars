# rbenv-set-vars

This is a plugin for [rbenv](https://github.com/sstephenson/rbenv),
used with the plugin
[rbenv-vars](https://github.com/sstephenson/rbenv-vars), making it
convenient to switch among different sets of environment variables.

## Installation

To install rbenv-set-vars, clone this repository into your
`~/.rbenv/plugins` directory. (You'll need a recent version of rbenv
that supports plugin bundles.)

    $ mkdir -p ~/.rbenv/plugins
    $ cd ~/.rbenv/plugins
    $ git clone https://github.com/YanhaoYang/rbenv-set-vars

## Usage

Define sets of environment variables in your project, with file names
like `.rbenv-vars-dev`, `.rbenv-vars-deploy`. For example, you may have
different BUNDLE_GEMFILE settings:

`.rbenv-vars-dev`:

    BUNDLE_GEMFILE=Gemfile_with_local_paths

`.rbenv-vars-deploy`

    BUNDLE_GEMFILE=Gemfile_with_git_urls

Having those files created, you can switch the environment varialbes
with commands like:

    rbenv set-vars dev
    rbenv set-vars deploy

Those commands simply create a symbol link to `.rbenv-vars-dev`,
`.rbenv-vars-deploy`. *Warn*: `.rbenv-vars` will be replaced by those
commands.

## Version History

* Initial public release.

## License

&copy; 2013 Yanhao Yang. Released under the MIT license. See
`LICENSE` for details.
