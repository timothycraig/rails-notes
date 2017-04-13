# rails-notes

### Rails new

```
rails new <app-name> --skip-bundle --database=postgresql --skip-turbolinks --skip-test-unit
rails new . --database=postgresql -T --skip-turbolinks
```

### Generators

```
rails g scaffold Blog title:string body:text
rails g controller Pages home about contact
rails g model Topic title:string
rails g resource Portfolio title:string subtitle:string body:text main_image:text thumb_image:text
rails g model Technology name:string portfolio:references
```

### Migrations

```
rails g migration AddPartNumberToProducts
rails g migration add_badge_to_skills badge:text
rails g migration add_topic_reference_to_blogs topic:references
```

### Routes

```
rake routes | grep search_term
```

### Rspec & capybara

```
rails g rspec:install

**rails_helper**

require 'spec_helper'
require 'rspec/rails'
require 'capybara/rails'
```

### Gems

```
group :development, :test do
  gem 'pry'
  gem 'byebug'
  gem 'rspec-rails'
  gem 'capybara'
  gem 'launchy'
  gem 'factory_girl_rails'
  gem 'orderly'
end

group :test do
  gem 'coveralls', require: false
end
```

#### Friendly IDs

```
rails generate friendly_id
rails g migration add_slug_to_blogs slug:string:uniq
```

#### Devise

```
rails generate devise:install
rails g devise:views
rails g devise User
```
