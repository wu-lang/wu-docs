# If and While

## If

In Wu, as mentioned, everything is an expression, even _if_-conditions. This means you can define your variables, call your functions etc. based on where the program flow is going.

Of course you can always decide to use vanilla if's:

```fsharp
if 2 + 2 == 2 {
  print("it's actually two")
} elif 2 + 2 == 3 {
  print("nevermind, it's three")
} else {
  print("I'm bad at addition")
}
```

Or not:

```fsharp
result := if 2 + 2 == 2 {
  "it's two"
} elif 2 + 2 == 3 {
  "it's three"
} else {
  "something else"
}

print(result)
```

## While

While-expressions work basically the same way as if-expressions, though they always return `()` - which is kind of useless, but for the sake of consistency and expression-oriented programming so whatever.

So, normal independent while loops:

```fsharp
a := 1
while a < 10 {
  print(a)
  a = a + 1
}
```

You can also assign variables to while loops, if you for some reason wanted to do that:

```fsharp
b := 1
a := while b == 1 {
  b = b - 1
}

# at this point `a` is nil :))
```

