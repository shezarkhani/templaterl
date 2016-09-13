[![Build Status](https://travis-ci.org/shezarkhani/templaterl.svg?branch=documentation)](https://travis-ci.org/shezarkhani/templaterl)

# templaterl
Simple templating with customizable expressions

# Usage
Simple replacement usage:
```erlang
templaterl:compile(<<"I have a {{{car_model}}}.">>, #{<<"car_model">> => <<"Nissan GTR">>})
```

# Tests
Run tests by running:
```
rebar3 eunit
```

# Benchmarks
You can run benchmarks on your own machine by running:
```bash
rebar3 cmd benchmark
```

Results:
```
TODO: Add benchmark results
```