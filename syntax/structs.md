# Structs

The following code shows basic use of a struct.

```fsharp
Point: struct {
    x: float
    y: float
}
```

{% hint style="info" %}
Comma separation is optional in struct initialization and definition.
{% endhint %}

`Point` is thus defined as a data structure containing two float fields `x`and `y`.

You can define instances of `Point`like so:

```fsharp
point0 := new Point {
    x: 100
    y: 200
}

point1: Point = new Point {
    x: 1
    y: 2
}
```

Struct fields are always mutable. You can access fields of a struct like this:

```fsharp
point := new Point {
    x: 100
    y: 100
}

point x = 20
point y = point x
```

{% hint style="info" %}
Wu does not use `.`for field access, because doing so would be gross.
{% endhint %}

We can also implement methods on our structs. This will feel very familiar for people with Rust experience.

```fsharp
Vector: struct {
    x: float,
    y: float
}

implement Vector {
    new: fun(x, y) -> Self {
        Vector {
            x: x,
            y: y
        }
    }

    length: fun(self) -> float {
        (self x^2 + self y^2)^0.5
    }

    normalize: fun(self) {
        len := self length()
        
        self x /= len
        self y /= len
    }
}

a := Vector new(100, 100)
a normalize()
```

{% hint style="info" %}
`Self` aliases whatever struct type you're implementing on.
{% endhint %}

