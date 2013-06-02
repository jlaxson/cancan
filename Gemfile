source "http://rubygems.org"

case ENV["MODEL_ADAPTER"]
when nil, "active_record"
  gem "sqlite3"
  gem "activerecord", '~> 4.0.0rc1', :require => "active_record"
  gem "with_model", "~> 0.2.5"
  #gem 'ransack',             github: 'ernie/ransack',            branch: 'rails-4'
  #gem 'meta_where'
when "data_mapper"
  gem "dm-core", "~> 1.0.2"
  gem "dm-sqlite-adapter", "~> 1.0.2"
  gem "dm-migrations", "~> 1.0.2"
when "mongoid"
  gem "bson_ext", "~> 1.1"
  gem "mongoid", "~> 2.0.0.beta.20"
else
  raise "Unknown model adapter: #{ENV["MODEL_ADAPTER"]}"
end

gem 'supermodel', github: 'maccman/supermodel'

gemspec
