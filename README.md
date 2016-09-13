[![Build Status](https://travis-ci.org/shezarkhani/templaterl.svg?branch=documentation)](https://travis-ci.org/shezarkhani/templaterl)

# templaterl
Simple templating with customizable expressions

# Usage
Simple replacement usage:
```erlang
templaterl:compile(<<"I have a {{{car_model}}}.">>, [{<<"car_model">>, <<"Nissan GTR">>}]).
<<"I have a Nissan GTR.">>
```

Replacement with expressions:
```erlang
Uppercase = "uppercase(_Token, Value) -> << <<(string:to_upper(X))>> || <<X>> <= Value >>.",
templaterl:register_helpers([Uppercase]),
templaterl:compile(<<"I have a {{{uppercase car_model}}}.">>, [{<<"car_model">>, <<"Nissan GTR">>}]).
<<"I have a NISSAN GTR.">>
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

# Profiling
To run and open qcachegrind on mac OSX:
```bash
rebar3 cmd profile
```