# Switch

Switch expressions work basically like `if`and can be used like the following:

```fsharp
a := compute_some_number()

switch a {
  | 0  => print("a is zero")
  | 10 => print("a is ten")
  | _  => print("something else")
}
```

And can be used as expressions:

```fsharp
foo: str = switch 10 {
  | 10 => "foo"
}
```

{% hint style="success" %}
Very nice.
{% endhint %}



