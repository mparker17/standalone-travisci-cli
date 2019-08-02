# standalone-travisci-cli

Compartmentalize Travis.CI's CLI.

# Prerequistes

1. Set up [rbenv][rbenv] and [ruby-build][ruby-build]:

        git clone https://github.com/rbenv/rbenv.git $HOME/.rbenv
        cd $HOME/.rbenv
        src/configure && make -C src
        # Add $HOME/.rbenv/bin to your $PATH, restart your shell.
        rbenv init
        # Follow instructions, restart your shell.
        mkdir -p $HOME/.rbenv/plugins
        git clone https://github.com/rbenv/ruby-build.git $HOME/.rbenv/plugins/ruby-build

[rbenv]: https://github.com/rbenv/rbenv
[ruby-build]: https://github.com/rbenv/ruby-build

# Install

1. Clone this repo.

        git clone --recursive git@github.com:mparker17/standalone-travisci-cli.git standalone-travisci-cli
        cd standalone-travisci-cli

2. Install Ruby, Bundler, and Travis.CI CLI:

        rbenv install
        gem install bundler
        bundle install

# Use

`bundle exec travis`

You probably want to start by logging in to Travis CI:

* If you want to work with an open-source repo, `bundle exec travis login`
* If you want to work with a closed-source repo, `bundle exec travis login --pro`

The first time that you ask Travis CLI to do something repository-specific, it will try (and fail) to auto-detect the repo:

        Detected repository as mparker17/standalone-travisci-cli, is this correct? |yes|

... answer `no`, and it will ask you for the actual repo:

        Detected repository as mparker17/standalone-travisci-cli, is this correct? |yes| no
        Repository slug (owner/name): |mparker17/standalone-travisci-cli|

... answer with your repo information.
