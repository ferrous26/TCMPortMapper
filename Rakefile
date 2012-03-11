task :default => :build

desc 'Build the TCMPortMapper framework'
task :build do
  sh 'xcodebuild -target TCMPortMapper'
  require 'fileutils'
  frameworks = File.expand_path '~/Library/Frameworks'
  FileUtils.rm_rf File.join(frameworks, 'TCMPortMapper.framework'), :verbose => true
  FileUtils.cp_r 'build/Release/TCMPortMapper.framework', frameworks, :verbose => true
end
