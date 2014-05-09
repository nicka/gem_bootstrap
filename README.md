## gem_bootstrap

[![Gem Version](https://badge.fury.io/rb/gem_bootstrap.svg)](http://badge.fury.io/rb/gem_bootstrap)
[![Dependency Status](https://gemnasium.com/agilecreativity/gem_bootstrap.png)](https://gemnasium.com/agilecreativity/gem_bootstrap)
[![Code Climate](https://codeclimate.com/github/agilecreativity/gem_bootstrap.png)](https://codeclimate.com/github/agilecreativity/gem_bootstrap)

Generate the starting template for creating the ruby gem in ruby in one command.

### Features:

- Test framework using [Minitest][]
- Document with [Yard][]
- Style check with [Rubocop][]
- Debug with [Pry][]
- Initial git commit with [Grit] gem
- Build on top of the most popular [Thor][] framework
- Give you simple working structure that you can build upon but not dictate on
  how you should do it
- Templates files are customizable to suite your specific need

### Requirements

#### Mandatory

- [Git][] the free and opensource distributed version control system.

### Optional

- Valid [Github][] account so that you can share your awesome gem with the community.

### Installation

Install the ruby gem

```sh
gem install gem_bootstrap
```

Then just run the `gem_bootstrap` without any argument for list of help

```
gem_bootstrap generate [GEM_NAME]
                       --github-id [GITHUB_ID]
                       --email [EMAIL]
                       --author [AUTHOR]
e.g.
gem_bootstrap generate awesome_gem
                       --github-id awesome_developer
                       --email cool@awesomedev.com
                       --author 'John Guru II'
gem_bootstrap help [COMMAND]  # Describe available commands or one specific command
gem_bootstrap usage           # Display help screen
```
To generate the gem just type the command like

```
gem_bootstrap generate awesome_gem --github-id awesome_developer -- email cool@awesomedev.com --author 'John Guru II'
```
Which should output something like

```
create  awesome_gem/README.md
create  awesome_gem/CHANGELOGS.md
create  awesome_gem/.yardopts
create  awesome_gem/.gitignore
create  awesome_gem/Gemfile
create  awesome_gem/Rakefile
create  awesome_gem/Guardfile
create  awesome_gem/.rubocop.yml
create  awesome_gem/rubocop-todo.yml
create  awesome_gem/awesome_gem.gemspec
create  awesome_gem/bin/awesome_gem
create  awesome_gem/lib/awesome_gem.rb
create  awesome_gem/lib/awesome_gem/version.rb
create  awesome_gem/lib/awesome_gem/logger.rb
create  awesome_gem/lib/awesome_gem/cli.rb
create  awesome_gem/lib/awesome_gem/awesome_gem.rb
create  awesome_gem/lib/awesome_gem/core_ext/hash/keys.rb
create  awesome_gem/test/test_helper.rb
create  awesome_gem/test/lib/awesome_gem/test_awesome_gem.rb
create  awesome_gem/LICENSE
```

```sh
# Change directory to the generated gem
cd awesome_gem

# Build the gem
bundle

# Run the default rake task (minitest and rubocop)
rake

# Install the gem to your local system
rake install

# You should have the basic command line that you can run like
awesome_gem
```

### Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

[Git]: http://git-scm.com/
[github]: https://github.com/
[Grit]: https://github.com/mojombo/grit
[Minitest]: https://github.com/seattlerb/minitest
[Thor]: https://github.com/erikhuda/thor
[Yard]: https://github.com/lsegal/yard
[Rubocop]: https://github.com/bbatsov/rubocop
[Pry]: https://github.com/pry/pry
