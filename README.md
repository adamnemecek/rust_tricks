# rust_tricks

## impl Into<Option<T>>
  
You have a function that takes an `Option<T>` but writing `f(Some(value))` instead of `f(value)` gets tedious. You can change the function to take `impl Into<Option<T>>` instead of `Option<T>` and then call it with `f(value)`.

Before: 
```rust
fn f(v: Option<u32>) { }

f(Some(10));
```

After:

```rust
fn f(v: impl Into<Option<u32>>) { }

f(10);
```



