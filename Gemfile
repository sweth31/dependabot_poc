source "https://rubygems.org"

git_source(:hp_instantink_git) { |repo_name| "git@github.azc.ext.hp.com:instantink/#{repo_name}.git" }

ruby "2.6.3"
gem "rails", "~> 6.1.3"
gem "json"

# Project Gems
gem "instantink_lib", hp_instantink_git: "instantink-lib"
# gem "instantink_lib", path: "../instantink-lib"
gem "omniauth-azure-activedirectory", hp_instantink_git: "ii_omniauth_azure_ad", branch: 'main'
# gem "omniauth-azure-activedirectory", path: "../ii_omniauth_azure_ad"
gem "faraday_connection", hp_instantink_git: "faraday_connection"
# gem "faraday_connection", path: "../faraday_connection"
gem "postcard", hp_instantink_git: "postcard"
# gem "postcard", path: "../postcard"

gem 'bookkeeper_client', hp_instantink_git:  'bookkeeper_client'
# gem 'bookkeeper_client', path: '../bookkeeper_client'

gem "aws-sdk-rails", require: false
gem "aws-sdk-sqs", require: false
gem "cancancan"
gem "data_migrate"
gem "devise"
gem "lograge"
gem "mysql2"
gem "net-ldap"
gem "nokogiri"
gem "paper_trail"
gem "rack-attack"
gem "rails_admin"
gem "remotipart"
gem "shoryuken"
gem "therubyracer"
gem "unicorn"

group :development, :test do
  gem "brakeman"
  gem "webdrivers"
  gem "factory_bot_rails"
  gem "rspec-rails"
  gem "selenium-webdriver"
  gem "simplecov", require: false
  gem "simplecov-rcov", require: false
end

group :development do
  gem "colored"
  gem "foreman"
  gem "git"
  gem "listen"

  # NOTE: Disabled spring because it messes up environment variables on initializers. Currently using one to conditionally set sqs client url
  # Spring speeds up development by keeping your application running in the background. Read more: https://github.com/rails/spring
  # gem "spring", "2.0.2"
  # gem "spring-watcher-listen", "2.0.1"
end

group :deployment, optional: true do
  gem "argos", hp_instantink_git: "argos", require: false
  # gem "argos", path: "../argos", require: false
  gem "aws-sdk-autoscaling"
  gem "capistrano", require: false
  gem "capistrano-bundler", require: false
  gem "capistrano-chef", require: false
  gem "capistrano-ext", require: false
  gem "capistrano-rails", require: false
  gem "capistrano-rvm", require: false
end

group :test do
  gem "capybara"
  gem "database_cleaner"
  gem "instantink_spec_helpers", hp_instantink_git: "instantink-spec-helpers"
  # gem "instantink_spec_helpers", path: "../instantink-spec-helpers"
  gem "launchy", require: false
  gem "rails-controller-testing"
  gem "shoulda-matchers"
  gem 'shammer', hp_instantink_git: 'shammer'
  # gem 'shammer', path: '../shammer'
  gem "webmock", require: false
end

# for assets:precompile
group :assets do
  gem "sqlite3"
end

group :code_review, optional: true do
  gem "rubocop-rspec", require: false
end
