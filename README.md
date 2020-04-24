# Cleversteam::Style

RuboCop implementation for Cleversteam projects. Based on [percy-style](https://github.com/percy/percy-style).

## Installation

Add this line to your application's Gemfile:

```ruby
group :test, :development do
  gem 'cleversteam-style'
end
```

Or for a Ruby gem/library, add this to your gemspec:

```ruby
spec.add_development_dependency 'cleversteam-style'
```

And then execute:

```bash
$ bundle install
```

## Usage

Create a file in your project root called `.rubocop.yml` with the following:

```yaml
inherit_gem:
  cleversteam-style:
    - default.yml
```

And then execute:

```bash
$ bundle exec rubocop
```

You do not need to include rubocop directly in your application's dependencies as this gem includes `rubocop` and `rubocop-rspec`.

## Releasing

To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).
