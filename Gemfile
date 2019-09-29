# frozen_string_literal: true

source "https://rubygems.org"
gemspec

gem "jekyll"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-paginate"
  gem 'jekyll-seo-tag'
  gem "jekyll-minifier"
  gem 'jekyll-admin', group: :jekyll_plugins
end

require 'rbconfig'
  if RbConfig::CONFIG['target_os'] =~ /darwin(1[0-3])/i
    gem 'rb-fsevent'
  end
