SpreePayoneFrontend
===================

Extends Spree for Supporting Payone Credit Card Payments via th payone FinanceGate Channel Frontend. An appropiate Payone Merchant Account is required to use it.


Installation
------------

Add spree_payone_frontend to your Gemfile:

```ruby
gem 'spree_payone_frontend', :git => 'git://github.com/hefan/spree_payone_frontend.git' 
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g spree_payone_frontend:install
```

Setup
-----

Navigate to Spree Backend/Configuraion/Payment Methods and add a new payment method with Provider "Spree::PaymentMethod::PayoneFrontend".

Enter the Portal id, the sub account id and the secret key from your payone account. Supported modes are "test" and "live".



Testing
-------

Be sure to bundle your dependencies and then create a dummy test app for the specs to run against.

```shell
bundle
bundle exec rspec spec
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_payone_frontend/factories'
```

Copyright (c) 2014 [name of extension creator], released under the New BSD License
