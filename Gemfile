source "https://rubygems.org"

# Mirrors the GitHub Pages build environment for local preview:
#   bundle install
#   bundle exec jekyll serve
gem "github-pages", "~> 232", group: :jekyll_plugins

# Required for `jekyll serve` on Ruby 3+
gem "webrick"

# Standard-library gems no longer bundled by default on Ruby 3.4+
gem "csv"
gem "bigdecimal"
gem "base64"
gem "logger"
gem "faraday-retry"

# Windows and JRuby do not include zoneinfo files
platforms :windows, :jruby do
  gem "tzinfo-data"
end
