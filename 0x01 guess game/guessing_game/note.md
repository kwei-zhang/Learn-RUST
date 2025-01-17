In Rust, variables are immutable by default, meaning once we give the variable a value, the value won’t change.
```
let apples = 5; // immutable
let mut bananas = 5; // mutable
```

The equal sign `(=)` tells Rust we want to bind something to the variable now. On the right of the equal sign is the value that guess is bound to, which is the result of calling `String::new`, a function that returns a new instance of a String.

io::stdin()
    .read_line(&mut guess)
    .expect("Failed to read line");
    ^
    variant(ok, err) but type?