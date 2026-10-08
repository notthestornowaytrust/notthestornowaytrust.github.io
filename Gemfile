source "https://rubygems.org"

# Match GitHub Pages' Jekyll version while allowing patched local plugins.
gem "jekyll", "~> 3.10.0"
gem "kramdown", "~> 2.4"
gem "kramdown-parser-gfm", "~> 1.1"
gem "rubyzip", ">= 3.4", "< 4"

# Ruby 3.4 supplies these safe_yaml and Liquid dependencies as separate gems.
gem "base64", "~> 0.3"
gem "bigdecimal", "~> 4.1"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-remote-theme", "~> 0.6.2"
end

group :development do
  gem "bundler-audit", "~> 0.9", require: false
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.0" if Gem.win_platform?
