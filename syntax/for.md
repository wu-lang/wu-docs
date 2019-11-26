# For

In Wu there are two different ways to use for loops. The first one is very simple:

```fsharp
for 100 {
  print("ONE HUNDRED TIMES!!!")
}
```

Simply using a single integer, you can repeat a certain code block a given amount of times.

The second way to use a for loop is using iterators. In the following snippet, we use the `range`built-in iterator:

```fsharp
for i in range(0, 100) {
  print("road to one hunnid: ", i)
}
```

Of course, enumerating iterators also exist:

```fsharp
numbers := [1, 2, 3, 4, 5]

for i, v in ipairs(numbers) {
  print(i, v)
}
```

Or simply iterating a list:

```fsharp
names := ["bob", "niels", "kaj"]

for v in iter(names) {
  print("name: " ++ name) 
}
```

