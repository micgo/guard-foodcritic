guard "bundler" do
  watch("Gemfile")
  watch(/^.+\.gemspec/)
end

guard "rspec", :version => 2, :cli=> "--format nested" do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$}) { |m| "spec/#{m[1]}_spec.rb" }
  watch("spec/spec_helper.rb") { "spec" }
  watch(%r{^spec/support/(.+)\.rb$}) { |m| "spec" }
end