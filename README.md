# draggable-rails
[![Gem Version](https://badge.fury.io/rb/draggable-rails.svg)](http://badge.fury.io/rb/draggable-rails)

draggable-rails gem is the integration of https://shopify.github.io/draggable/ javascript library for your Rails 4 and Rails 5 application.

The JavaScript Drag & Drop library your grandparents warned you about. 
source: https://shopify.github.io/draggable/

Ruby gems url: https://rubygems.org/gems/draggable-rails

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'draggable-rails'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install draggable-rails

Now you need to edit your `app/assets/javascripts/application.js` file and add the following line:

``` javascript
//= require draggable
```

## Example code:

Working example code for draggable li element you can see the event changes in the browser console.

Note: I am using jQuery.

You can add a script.js file `app/assets/javascripts/script.js` and add the following line:

``` javascript

$(document).on("turbolinks:load", function() {	  

  new Draggable.Draggable(document.querySelectorAll('ul'), {
    draggable: 'li'
  })
  .on('drag:start', () => console.log('drag:start'))
  .on('drag:move',  () => console.log('drag:move'))
  .on('drag:stop',  () => console.log('drag:stop'));
});

```

index.html.erb file `app/views/pages/index.html.erb` and add the following line:

``` html
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
```

## Usage Full documentation 

Read the Shopify draggable.js documentation here https://github.com/Shopify/draggable

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake false` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/sadiqmmm/draggable-rails. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

