require 'bundler'
Bundler::GemHelper.install_tasks

require 'spree/testing_support/extension_rake'

task :default do
  if Dir["spec/dummy"].empty?
    Rake::Task[:test_app].invoke
    Dir.chdir("../../")
  end
  Rake::Task[:spec].invoke
end

desc 'Generates a dummy app for testing'
task :test_app do
  ENV['LIB_NAME'] = 'spree_klaviyo'
  Rake::Task['extension:test_app'].invoke
end
