# README

This is an example InterMine for demo and testing.

It's used by the [tutorial](http://intermine.readthedocs.io/en/latest/get-started/tutorial), and we use it for our continuous integration tests on [Travis](https://travis-ci.org/intermine/intermine/builds)

# Building the mine

This mine can be built with the `./setup.sh` script.  Steps:

1. Install Perl module dependencies: `sudo cpan XML::Parser::PerlSAX Text::Glob Cwd Getopt::Std`
1. Install and start postgresql on your system
1. Install tomcat but don't start it, as the build script will handle this for you
1. Create an `.intermine` directory in your $HOME directory
1. Copy [biotestmine.properties](https://github.com/intermine/biotestmine/blob/master/data/biotestmine.properties) into the  `~/.intermine` directory
1. Replace PSQL_USER and PSQL_PWD with your postgres username and password.
1. (Optional) Initialise the two search repositories used by InterMine. If you don't do this, the keyword search won't work in your mine. Follow the instructions for [Solr](https://intermine.readthedocs.io/en/latest/system-requirements/software/solr/)
1. Run build script in your `biotestmine` repository: `./setup.sh`
