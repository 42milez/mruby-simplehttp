# SimpleHttp Class for mruby
refactored SimpleHttp using mruby-uv and mruby-http

original code is iij/mruby 

## install by mrbgems
```bash
git clone git://github.com/matsumoto-r/mruby-simplehttp.git
cp -pr mruby-simplehttp ${MRUBY_ROOT}/mrbgems/g/.
echo mruby-simplehttp >> ${MRUBY_ROOT}/mrbgems/GEMS.active
cd ${MRUBY_ROOT}
make
./bin/mruby ${MRUBY_ROOT}/mrbgems/g/mruby-simplehttp/example/get.rb
```

## example

```ruby
p SimpleHttp.new("127.0.0.1", 80).request("GET", "/index.html", {'User-Agent' => "test-agent"})
```

