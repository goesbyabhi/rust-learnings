# Day 1
1) A `match` type compares and automatically outputs the result
2) `String` and `str` are not the same
3) Pass everything by reference `&`
4) We use `let` to declare a variable and this variable is not mutable by default
5) To make it mutable, we add the `mut` keyword
6) Understand the different types of imports
```rust
use ran::Rng;
let secret_number = rand.thread_rng().gen_range(1..=100); // We use Rng trait, and then we use rand.{function within the Rng trait's scope}

use rand::{thread_rng, Rng};
let secret_number = thread_rng().gen_range(1..100); // We import thread_rng from rand and gen_range is a part of Rng
```
7) To change a mutable variable later, we will still have to do let {var};
8) Rust focuses a lot on Error handling so wherever there's a `Result` type, we use `.expect("Message")` to point out errors OR
we use `match` keyword in the beginning to segregate Ok and Err messages like this
```rust
let guess: u32 = match guess.trim().parse() {
    Ok(num) => num,
        Err(_) => continue,
};
```
with expect it would be like this
```rust
let guess: u32 = guess.trim().parse().expect("Please type a number!");
```

