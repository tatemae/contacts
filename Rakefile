require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "muck-contacts"
  gem.homepage = "http://github.com/tatemae/contacts"
  gem.license = "MIT"
  gem.summary = %Q{A universal interface to grab contact list information from various providers including Outlook, Address Book, Yahoo, AOL, Gmail, Hotmail, and Plaxo.}
  gem.description = %Q{A universal interface to grab contact list information from various providers including Outlook, Address Book, Yahoo, AOL, Gmail, Hotmail, and Plaxo.}
  gem.email = "rob@notch8.com"
  gem.authors = ["Rob Kaufman"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  #  gem.add_runtime_dependency 'jabber4r', '> 0.1'
  #  gem.add_development_dependency 'rspec', '> 1.2.3'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/*_test.rb'
  test.verbose = true
end

#require 'rcov/rcovtask'
#Rcov::RcovTask.new do |test|
  #test.libs << 'test'
  #test.pattern = 'test/**/test_*.rb'
  #test.verbose = true
#end

task :default => :test
