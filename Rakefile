require 'rubygems'
require 'bundler/setup'
require 'html-proofer'

desc 'Test the html.'
task :test do
  sh 'bundle exec jekyll build --trace'
  HTMLProofer.check_directory(
    './_site',
    check_html: true,
    validation: {
      report_missing_names: true,
      report_script_embeds: true
    }
  ).run
end

task default: :test
