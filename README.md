

# Erlang LRU: a fixed size LRU cache. #

Copyright (c) 2015 Benoît Chesneau.

__Version:__ 1.3.1.

## Erlang LRU

Erlang LRU implements a fixed size [LRU cache](https://en.wikipedia.org/wiki/Cache_algorithms#LRU).

The cache is maintained in a process that could be added to a supervision tree.

Usage:
------

Its usage is very simple.

```erlang

Size = 128,
{ok, Cache} = lru:start(Size),

lru:add(Cache, 1, 1),
lru:add(Cache, 2, 2),
lru:remove(Cache, 2),

...
```

## Documentation

Full doc is available in the [`lru`](http://github.com/barrel-db/erlang-lru/blob/master/doc/lru.md) module.

## Build

```
$ rebar3 compile
```

