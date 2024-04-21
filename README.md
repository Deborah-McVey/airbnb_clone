"Let's Build Airbnb with Ruby on Rails" by TypeFast (67 parts), Aug. 23, 2022
https://www.youtube.com/playlist?list=PLCawOXF4xaJK1_-KVgXyREULRVy_W_1pe

sudo apt install libpq-dev
sudo apt install postgresql
bundle i

rails new airbnb_clone -T -d postgresql --css tailwind

gem 'devise'
gem 'rspec-rails' in testing
bundle i
bundle exec rails s 
rails g devise:install
rails g rspec:install

https://github.com/rspec/rspec-rails

Depending on your application's configuration some manual setup may be required:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

     * Required for all applications. *

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"
     
     * Not required for API-only Applications *

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

     * Not required for API-only Applications *

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views
       
     * Not required *

rails g devise User     

rails db:migrate