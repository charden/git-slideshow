guard 'shell' do
  watch(/index.md/) {|m|
    `slideshow b #{m[0]} -t shower ` }
end
guard 'livereload' do
  watch (%r{index.html})
end
