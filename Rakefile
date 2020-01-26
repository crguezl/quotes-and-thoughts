desc "Publicar en GitHub el Blog"
task :default do
  sh "git ci -am 'thoughts' && git push"
end

desc "serve locally"
task :serve do
  sh "bundle exec jekyll serve --future --watch --port 8083"
end

require 'html-proofer'
desc "test links in the build web site"
task :test do
  sh "bundle exec jekyll build"
  options = { 
    :assume_extension => true, 
    :disable_external => true, 
    :empty_alt_ignore => true,
    :file_ignore => [ %r{categories} ]
  }
  HTMLProofer.check_directory("./_site", options).run
end