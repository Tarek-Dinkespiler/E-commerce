# frozen_string_literal: true

source 'https://rubygems.org'
git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?('/')
  "https://github.com/#{repo_name}.git"
end

File.read('./.ruby-version')

gem 'bootsnap', '>= 1.1.0', require: false
gem 'coffee-rails', '~> 4.2'
gem 'figaro', '~> 1.1', '>= 1.1.1'
gem 'font-awesome-rails', '~> 4.7', '>= 4.7.0.4'
gem 'jbuilder', '~> 2.5'
gem 'jquery-rails', '~> 4.3', '>= 4.3.3'
gem 'pg', '>= 0.18', '< 2.0'
gem 'puma', '~> 3.11'
gem 'rails', '~> 5.2.1', '>= 5.2.1.1'
gem 'sass-rails', '~> 5.0'
gem 'turbolinks', '~> 5'
gem 'uglifier', '>= 1.3.0'

group :development, :test do
  gem 'factory_bot_rails', '~> 4.0'
  gem 'faker', '~> 1.8', '>= 1.8.7'
  gem 'pry-byebug', '~> 3.6'
  gem 'rspec-rails', '~> 3.7', '>= 3.7.2'
  gem 'sandi_meter', '~> 1.2'
end

group :development do
  gem 'annotate', '~> 2.7', '>= 2.7.4'
  gem 'husky', '~> 0.5.15'
  gem 'listen', '>= 3.0.5', '< 3.2'
  gem 'rubocop', '~> 0.60.0', require: false
  gem 'rubocop-rspec', '~> 1.30', '>= 1.30.1', require: false
  gem 'spring', '~> 2.0', '>= 2.0.2'
  gem 'spring-watcher-listen', '~> 2.0.0'
end

group :test do
  gem 'database_cleaner', '~> 1.7'
  gem 'shoulda-matchers', '~> 3.1'
  gem 'simplecov', '~> 0.16.1', require: false
end

gem 'tzinfo-data', platforms: %i[mingw mswin x64_mingw jruby]
