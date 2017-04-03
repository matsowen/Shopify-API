# Shopify-API
Shopify API development.

************************

gem: https://img.shields.io/gem/v/shopify_api.svg
gem_url: https://rubygems.org/gems/shopify_api

**********************************************************************************************************

The Shopify API gem allows Ruby developers to programmatically access the admin section of Shopify stores.

The API is implemented as JSON over HTTP using all four verbs (GET/POST/PUT/DELETE). Each resource, like Order, Product, or Collection, has its own URL and is manipulated in isolation. In other words, we’ve tried to make the API follow the REST principles as much as possible.

## Usage

### Requirements

All API usage happens through Shopify applications, created by either shop owners for their own shops, or by Shopify Partners for use by other shop owners:

* Shop owners can create applications for themselves through their own admin: https://docs.shopify.com/api/authentication/creating-a-private-app
* Shopify Partners create applications through their admin: http://app.shopify.com/services/partners

For more information and detailed documentation about the API visit http://api.shopify.com

#### Ruby version

This gem requires Ruby 2.3.1 as of version 4.3. If you need to use an older Ruby version then update your `Gemfile` to lock onto an older release than 4.3.

### Installation

Add `shopify_api` to your `Gemfile`:

```ruby
gem 'shopify_api'
```

Or install via [gem](http://rubygems.org/)

```bash
gem install shopify_api
```

#### Rails 5

shopify_api is compatible with Rails 5 but since the latest ActiveResource release (4.1) is locked on Rails 4.x, you'll need to use the unreleased master version:

```ruby
gem 'shopify_api'
gem 'activeresource', github: 'rails/activeresource'
```

### Console

This package also supports the ``shopify-cli`` executable to make it easy to open up an interactive console to use the API with a shop.

1. Install the ``shopify_cli`` gem.

```bash
gem install shopify_cli
```

2. Obtain a private API key and password to use with your shop (step 2 in "Getting Started")

3. Use the ``shopify-cli`` script to save the credentials for the shop to quickly log in.

   ```bash
   shopify-cli add yourshopname
   ```

   Follow the prompts for the shop domain, API key and password.

4. Start the console for the connection.

   ```bash
   shopify-cli console
   ```

5. To see the full list of commands, type:

   ```bash
   shopify-cli help
   ```

## Threadsafety

ActiveResource is threadsafe as of version 4.1 (which works with Rails 4.x and above).

If you were previously using Shopify's [activeresource fork](https://github.com/shopify/activeresource) then you should remove it and use ActiveResource 4.1.

## Using Development Version

Download the source code and run:

```bash
rake install
```

## Additional Resources

API Docs: http://docs.shopify.com/api

Ask questions on the forums: http://ecommerce.shopify.com/c/shopify-apis-and-technology

## Copyright

Copyright (c) 2016 11 customized by Mats.
