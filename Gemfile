source "https://rubygems.org"
ruby File.read(".ruby-version").strip

=begin 
`find_spec_for_exe': can't find gem rake (>= 0.a) with executable rake
(Gem::GemNotFoundException)
from /opt/hostedtoolcache/Ruby/3.3.0/x64/lib/ruby/3.3.0/rubygems.rb:278:in
`activate_bin_path'
	from /opt/hostedtoolcache/Ruby/3.3.0/x64/bin/rake:25:in `<main>'
=end
# See https://github.com/protocolbuffers/protobuf/pull/15203
gem "rake", "~> 13.2.0"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
gem "jekyll","~> 4.3.3", group: :jekyll_plugins

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", github: 'jekyll/minima', branch: "master"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
#gem "github-pages", "~> 228", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17.0"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.2.0", :install_if => Gem.win_platform?

# kramdown v2 ships without the gfm parser by default. If you're using
# kramdown v1, comment out this line.
gem "kramdown-parser-gfm"

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
