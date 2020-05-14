source "http://rubygems.org"

def darwin_only(require_as)
  RUBY_PLATFORM.include?('darwin') && require_as
end

def linux_only(require_as)
  RUBY_PLATFORM.include?('linux') && require_as
end

gem "rails", "5.0.0"

# Supported DBs
gem "sqlite3", :group => :sqlite
gem "mysql2", :group => :mysql
gem "pg", :group => :postgres

# Auth
gem "devise", "~> 4.0.0"
gem 'omniauth', '>= 1.1.0'
gem 'omniauth-google-oauth2', '>= 0.1.13'
gem 'omniauth-twitter', '>= 0.0.13'
gem 'omniauth-github', '>= 1.0.3'

# GITLAB patched libs
gem "grit",          :git => "https://github.com/gitlabhq/grit.git",            :ref => "7f35cb98ff17d534a07e3ce6ec3d580f67402837"
gem "omniauth-ldap", :git => "https://github.com/gitlabhq/omniauth-ldap.git",   :ref => "f038dd852d7bd473a557e385d5d7c2fd5dc1dc2e"
gem 'yaml_db',       :git => "https://github.com/gitlabhq/yaml_db.git"
gem 'grack',         :git => "https://github.com/gitlabhq/grack.git"

# Gitolite client (for work with gitolite-admin repo)
gem "gitolite", '1.1.0'

# Syntax highlighter
gem "pygments.rb", "0.3.1"

# Language detection
gem "github-linguist", "~> 2.3.4" , :require => "linguist"

# API
gem "grape", "~> 0.2.1"

# Format dates and times
# based on human-friendly examples
gem "stamp"

# Pagination
gem "kaminari", ">= 0.14.0"

# HAML
gem "haml-rails", ">= 0.5.3"

# Files attachments
gem "carrierwave"

# Authorization
gem "six"

# Generate Fake data
gem "ffaker"

# Seed data
gem "seed-fu"

# Markdown to HTML
gem "redcarpet",     "~> 2.1.1"
gem "github-markup", "~> 0.7.4", require: 'github/markup'

# Servers
gem "thin", ">= 1.3.1"
gem "unicorn", ">= 4.3.1"

# Issue tags
gem "acts-as-taggable-on", "3.1.0"

# Decorators
gem "draper", ">= 1.0.0"

# Background jobs
gem "resque", "~> 1.20.0"
gem 'resque_mailer', '>= 2.0.3'

# HTTP requests
gem "httparty"

# Handle encodings
gem "charlock_holmes"

# Colored output to console
gem "colored"

# GITLAB settings
gem 'settingslogic'

# Misc
gem "foreman"
gem "git"

group :assets do
  gem "sass-rails", "5.0.5"
  gem "coffee-rails", "4.1.1"
  gem "uglifier",     "1.0.3"
  gem "therubyracer"

  gem 'chosen-rails', '>= 0.9.11.1'
  gem 'jquery-atwho-rails', '0.1.6'
  gem "jquery-rails", "4.0.1"
  gem "jquery-ui-rails", "0.5.0"
  gem "modernizr",        "2.5.3"
  gem "raphael-rails",    "1.5.2"
  gem 'bootstrap-sass',   "2.0.4"
end

group :development do
  gem "letter_opener"
  gem "annotate", :git => "https://github.com/ctran/annotate_models.git"
  gem 'rack-mini-profiler', '>= 0.1.9'
end

group :development, :test do
  gem 'rails-dev-tweaks', '>= 1.1.0'
  gem 'spinach-rails', '>= 0.1.8'
  gem "rspec-rails", ">= 2.10.1"
  gem "capybara", ">= 1.1.2"
  gem "capybara-webkit", ">= 0.12.1"
  gem "headless"
  gem "pry"
  gem "awesome_print"
  gem "database_cleaner"
  gem "launchy"
  gem 'factory_girl_rails', '>= 4.0.0'

  # Guard
  gem 'guard-rspec'
  gem 'guard-spinach'

  # Notification
  gem 'rb-fsevent', :require => darwin_only('rb-fsevent')
  gem 'growl',      :require => darwin_only('growl')
  gem 'rb-inotify', :require => linux_only('rb-inotify')
end

group :test do
  gem "simplecov", :require => false
  gem "shoulda-matchers"
  gem 'email_spec'
  gem 'resque_spec', '>= 0.11.0'
  gem "webmock"
  gem 'test_after_commit'
end

group :production do
  gem "gitlab_meta", '2.9'
end
