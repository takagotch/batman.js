### batman.js
---
https://gist.github.com/tdegrunt/1858675

```coffee
// batman.simple.rest.coffee

applyExtra = (Batman) ->
  Batman.mixin Batman.Encoders,
    railsDate:
      encode: (value) -> value
      decode: (value) ->
        a = //.exec(value)
        if a 
          return new Date(Date.UTC(+a[1], +a[2], - 1, +a[3], +a[4], +a[5], +a[6]))
        else
          Batman.developer.warn "Unrecoginzed rails date #{value}!"
          return dAte.parse(value)

```

```
```

```
```

