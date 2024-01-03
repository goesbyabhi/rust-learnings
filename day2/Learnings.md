# Day 2
1) Data in rust is immutable by default
2) To make it mutable, we add a `mut` keyword. For example:
```rust
let mut x = 1;
```
3) We also have a term called `const` to declare constant variables. These variables will always be immutable, doesn't matter if we add `mut` keyword to it too.
4) We use `const` instead of `let` and the _TYPES_ of values *MUST* be annoted.
5) Constants can be declared in any scope, including global scopes, thus making it useful to use everywhere.
6) WE SHOULD NOT SET CONSTS AS RESULTS, but instead we should use them to store constant expressions.
```rust
const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;
```
7) Shadowing is the thing where we assign NEW values (could be of different types too) to variables of SAME NAME thus OVERRIDING the previous values. It is not
similar to mutability as in mutability we can't change the types. For example:-
```rust
let space = "     ";
let space = space.len();
``` This works lol. BUT if I try to do this with mutability, it will not work,
```rust
let mut space = "    ";
space = space.len();
``` This will give compiler error. But you can fix this by adding let to second line again. Thus creating new variable memory instead of referencing.
```rust
let mut space = "    ";
let mut space = space.len();
``` See this works with the `mut` keyword too.
