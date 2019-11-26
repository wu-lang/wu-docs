# Traits

Wu has straight up stolen trait behavior from Rust and Pony. Traits can be thought of as behavior criteria for a struct, defined as a set of methods one can expect to find on a struct.

A trait can be defined like so:

```fsharp
Movable: trait {
    move: fun(self, dx: float, dy: foat)
}
```

Thus, anything that implements `Movable`will have to have a method named `move`that takes the given parameters on it.

We can implement traits on a struct like this:

```fsharp
Vector: struct {
    x: float
    y: float
}

implement Vector: Movable {
    move: fun(self, dx: float, dy: float) {
        self x += dx
        self y += dy   
    }
}
```

Now, when we try to move a `Vector` using the `move`method it works perfectly:

```fsharp
point := new Vector {
    x: 100
    y: 100
}

point move(10, 5)
```



