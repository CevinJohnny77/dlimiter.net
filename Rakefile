task :default => [:deploy]

task :generate do
    system "jekyll"
end

task :server do
    system "jekyll --server --auto"
end

task :deploy => [:generate] do
    sh "rsync -av --rsh='ssh -p 2683' _site/ dlimiter@crimsoncactus.net:public_html/"
end
