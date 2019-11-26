# Declarations

> "Like most languages I can think of, Wu's data handling is highly based around the concept of variables." - Bruce Lee

## Primitives

Variables are highly dependent on types to decide what they want inside them:

```rust
fruit: str = "milk"
fruit = 10
```

As the smart reader might realize, this code is invalid in the way that it's not okay to store numbers in a `str`.

By omitting types in you variable declarations, it doesn't mean the variable won't have a type; you simply pass on the job of figuring out the type onto the compiler.

```fsharp
favorite_number: int = 0  # an int, pff
least_favorite := 100     # also an int ?!
```

Now would you take a look at all these amazing types:

```fsharp
weight:  int   = 83
height:  float = 187.75
name:    str   = "neils"
letter:  char  = 'u'
uses_wu: bool  = true
```

## Casting

Of course, to prevent weird behavior in Wu programs, it's illegal by default to operate values of different types than what is expected. In special scenarios though, it's super useful to be able to use a value as something it isn't\(or might be\).

This is done using the `as` keyword:

```fsharp
# this will cold-bloodedly floor 10.5 to 10
banana: int = 10.5 as int
```

With great power comes great responsibility ... the latter, Wu won't bother you with, thus you might get _constructive critique_ for casting things which should not be cast.

```rust
banana: int = "100" as int
```

```text
wrong: can't cast `str` to `int`
     --> projects/spiderman.wu
      │
    1 │ banana: int = "100" as int
      |
```

## Splats

You can declare multiple values at once like the following:

```fsharp
a, b := 1, 2
```

These are also useful for returning multiple values:

```fsharp
foo: fun {
  1, 2
}

bar: fun {
  return 1, 2
}
```



