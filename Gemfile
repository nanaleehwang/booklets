source "https://rubygems.org"

gem "jekyll", "~> 4.3.0"
gem "minima", "~> 2.5"

# Ruby 3.4+ compatibility gems
gem "csv"
gem "logger"
gem "base64"
gem "erb"
gem "ostruct"
gem "bigdecimal"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

platforms :windows do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:windows]
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]