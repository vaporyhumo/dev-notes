# Scripting with ruby
### Using bundler inline
Como usar gemas desde dentro de un script sin tener que instalarlas antes.
[https://nithinbekal.com/posts/bundler-inline-gemfile/](https://nithinbekal.com/posts/bundler-inline-gemfile/)

```ruby
require 'bundler/inline'

gemfile do
  source 'https://rubygems.org'
  gem 'benchmark-ips', require: 'benchmark/ips'
end

Benchmark.ips do |x|
  x.report('original') { naive_implementation() }
  x.report('optimized') { fast_implementation() }

  x.compare!
end
```
