# Optionals

Optional variable types are types that are allowed to contain a `nil` values:

```fsharp
foo: int? = 10
foo = nil
foo = 100
```

{% hint style="info" %}
Optional types are denoted by a `?`
{% endhint %}

We can safely unwrap an optional value, given that it exists, using `!`like this:

```fsharp
foo: str? = maybe_a_str()
bar: str = foo!
```

