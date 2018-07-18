source "https://rubygems.org"

gemspec

if RUBY_VERSION =~ /^1\.8/ || RUBY_VERSION =~ /^1\.9\.[012]$/
  gem 'rake', '~> 10.5.0'
else
  gem 'rake', '~> 11.0'
end

# Pin this version since Rubocop occasionally adds new cops in
# incremental releases and we don't want out builds going red because
# of that.
gem 'rubocop', '= 0.33.0'

gem 'minitest', '>= 5.0.0', '< 6.0.0', :group => :test
# gem "sass-spec", :path => "../sass-spec"
gem "sass-spec", :git => 'https://github.com/sass/sass-spec.git', :branch => 'master'

# Removed from standard library in Ruby 2.5.0.
if Gem::Version.new(RUBY_VERSION) >= Gem::Version.new('2.5.0')
  gem 'mathn'
end
