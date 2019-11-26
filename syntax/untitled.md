# Module

Modules are simply scopes of code, that can be indexed like struct instances:

```fsharp
farm: module {
  cow := "moo"
  cat := "mooo"
  fish := "blob"
}

favorite_sound := farm fish
```



