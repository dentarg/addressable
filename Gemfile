# frozen_string_literal: true

source 'https://rubygems.org'

gemspec

group :test do
  gem 'bigdecimal' if RUBY_VERSION > '2.4'
  gem 'rspec'
  gem 'rspec-its'
end

group :coverage do
  gem "coveralls", "> 0.7", require: false, platforms: :mri
  gem "simplecov", require: false
end

group :development do
  gem 'launchy', '~> 2.4', '>= 2.4.3'
  gem 'redcarpet', :platform => :mri_19
  gem 'yard'
end

group :test, :development do
  gem 'memory_profiler'
  gem "rake", ">= 12.3.3"
end

unless ENV["IDNA_MODE"] == "pure"
  gem "idn-ruby", platform: :mri
end
