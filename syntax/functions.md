# Functions

Wu functions are expressions, but can also be declared using the same notation as `struct`. For example we can declare functions like this:

```fsharp
add_two: fun(a: int) {
    a += 2
}
```

The following is just as valid, but more ugly:

```fsharp
add_two := fun(a: int) {
    a += 2
}
```

{% hint style="info" %}
They are the exact same behind the scenes. No difference at all.
{% endhint %}

Functions return the last expression in their body implicitly\(like in Rust\) like so:

```fsharp
ten: fun {
    10
}

print(ten()) # 10
```

{% hint style="info" %}
Why have parentheses if they're empty anyways?
{% endhint %}

You are still able to use explicit returns:

```fsharp
twenty: fun {
    return ten() + ten()
}
```

Of course, as we're dealing with a decent language, higher order functions are a thing:

```fsharp
apply: fun(f: fun(int) -> int, a: int) -> int {
    f(a)
}

# 12
apply(fun(a: int) { a + 2 }, 10)
```

Now for something vaguely interesting. Splats are basically a catchall parameter, that binds as many arguments you throw at it into an array:

```fsharp
choose_first: fun(things: ...) -> any {
    things[0]
}

a := choose_first(1, 2, 3, 4, 5, 6)

print(a) # 1
```

Of course we can type the splats:

```fsharp
choose_second: fun(floats: ...float) -> float {
    floats[1]
}

a := choose_second(1.0, 2.1, 3.8)

print(a) # 2.1
```

