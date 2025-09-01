source "https://rubygems.org"
gemspec

case redis_version = ENV.fetch('REDIS_VERSION', 'latest')
when 'latest'
  # Pin to < 5.4.1 due to load order bug with Redis::NoScriptError
  # See: https://github.com/redis/redis-rb/issues/1321
  gem 'redis', '~> 5.0', '< 5.4.1'
else
  gem 'redis', "~> #{redis_version}.0"
end

rack_version = ENV.fetch('RACK_VERSION', '2')
gem "rack", "~> #{rack_version}.0"

gem "benchmark"
gem "json"
gem "minitest", "~> 5.11"
gem "mocha", "~> 2.0", require: false
gem "ostruct"
gem "pry"
gem "rack-test", "~> 2.0"
gem "rake"
gem "rubocop", "~> 0.80"
