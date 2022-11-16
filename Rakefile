require 'rake'
require 'parallel'
require 'cucumber/rake/task'

task default: :single

task :test do |_t, _args|
  Rake::Task['single'].invoke
  Rake::Task['single'].reenable
end

task :single, [:tag] do |_t, args|
  Cucumber::Rake::Task.new(:features) do |task|
    ENV['CONFIG_NAME'] ||= 'single'
    task.cucumber_opts = %w[--format=pretty features/single.feature]
    task.cucumber_opts << ["--tags @#{args[:tag]}"] unless args[:tag].nil?
    task.cucumber_opts << ['-f junit -o ./reports/report_xml'] unless ENV['xml'].nil?
    task.cucumber_opts << ['-f html -o ./reports/report_html.html'] unless ENV['html'].nil?
  end
  Rake::Task[:features].invoke
end