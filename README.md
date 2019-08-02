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
