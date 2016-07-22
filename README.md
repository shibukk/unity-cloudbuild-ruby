# Unity::Cloudbuild

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/unity/cloudbuild`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'unity-cloudbuild'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install unity-cloudbuild

## Usage

### Basic usage

The gem uses a client model to query against the API of Unity Cloud Build.
First of all, you create and configure a client through that.

```ruby
Unity::Cloudbuild.client.configure do |config|
  config.token   = "YOUR_TOKEN"
  config.org     = "YOUR_ORG"
  config.project = "YOUR_PROJECT"
end
```

### Build

If you want to build any, you can use `#build` with a build_target.

```ruby
Unity::Cloudbuild.client.build(build_target: "YOUR_BUILD_TARGET")
```

### Cancel

If you want to cancel build still in progress, you can use `#cancel` with a build_target.

```ruby
Unity::Cloudbuild.client.cancel(build_target: "YOUR_BUILD_TARGET")
```

Click here to read more information on the API.  
https://build-api.cloud.unity3d.com/docs/1.0.0/index.html.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/unity-cloudbuild. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
