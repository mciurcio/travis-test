require 'English'
require 'rubocop/rake_task'

RuboCop::RakeTask.new

desc 'Validate shell script installer'
task :validate_installer do
  system('shellcheck puppet-agent-installer.sh')
  raise 'Violations found using ShellCheck' unless $CHILD_STATUS.success?
end

task :default => [:rubocop]
