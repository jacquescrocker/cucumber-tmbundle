$:.unshift(File.dirname(__FILE__) + '/../../rspec/lib')
require 'rubygems'
require 'rspec/core/rake_task'

desc "Run all specs"
Rspec::Core::RakeTask.new do |t|
  t.spec_files = FileList['Support/spec/**/*_spec.rb']
  t.rcov = true
  t.spec_opts = ['--colour', '--diff']
  t.rcov_opts = ['--exclude', 'TextMate.app,gem,rspec\/plugins,rspec\/lib\/spec,spec\/spec,fixtures,bin\/spec']
end

task :default => :spec

Dir['Support/bundle_tasks/**/*.rake'].each { |rake| load rake }
