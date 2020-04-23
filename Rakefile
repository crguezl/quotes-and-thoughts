desc "Publicar en GitHub "
task :default do
  sh "git ci -am 2019 && git push"
end

desc "serve locally"
task :serve do
  sh "bundle exec jekyll serve --future --watch --port 8083 -H 0.0.0.0"
end

