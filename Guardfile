guard 'shell' do
  watch(/git.md/) {|m|
    `slideshow b #{m[0]} -t shower ` }
end
guard 'livereload' do
  watch (%r{git.html})
end
