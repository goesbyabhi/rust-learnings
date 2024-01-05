# Day 4
1) You declare a function using the `fn` keyword.
2) The function must have a parameter type if it is taking any parameters.
3) Statements are just some instructions that perform some code action but do not return a value.
```rust
    let x = 6;
```
This is a statement. Whenever we use `let` keyword, we are using a statement.
4) We cannot re-assign two statement. For example how we do `x = y = 2` in other languages, we can't do it in rust.
5) An expression is something that returns a value.
6) An expression doesn't have a semi-colon in the end. If you add one, it becomes a statement.
```rust
fn main() {
    let y = {
        let x = 5; // A statement
        x + 1 // An expression
    };
    println!("The value of y is: {y}");
}
```

```rust
fn five() -> i32 {
    5
}

fn main() {
    let x = five();

    println!("The value is : {x}");
}
```
7) We add new comments by adding // and then it becomes a comment. This is the idiomatic style.
8) There is some documentation comments too, just like JSDoc but it will be in some future section
9) We can do if, else if, else in the following way
```rust
fn main() {
    let number = 6;

    if number % 4 == 0 {
        println!("number is divisible by 4");
    } else if number % 3 == 0 {
        println!("number is divisible by 3");
    } else if number % 2 == 0 {
        println!("number is divisible by 2");
    } else {
        println!("number is not divisible by 4, 3, or 2");
    }
}
```
10) Using `if` in a `let` statement:
```rust
fn main() {
    let condition = true;
    let number = if condition { 5 } else { 6 }; // If condition is true then 5 else 6

    println!("The value of number is: {number}");
}
```
11) You can create an infinite loop using the `loop` keyword but you will have to explictly stop it using Ctrl-c or `break` keyword. We can use `continue` to skip over a particular loop.
```rust
fn main() {
    loop {
        println!("Lol");
    }
}
```
12) We can add labels to our `loop` to differentiate between various loops.
```rust
fn main() {
let mut count = 0;
'counting_up: loop {
    println!("count = {count}");
    let mut remaining = 10;

    loop {
        println!("remaining = {remaining}");
        if remaining == 9 {
            break;
        }
        if count == 2 {
            break 'counting_up;
        }
        remaining -= 1;
    }

    count += 1;
}
println!("End count = {count}");
}
```
13) You can use `while` loops too
```rust
fn main() {
    let a = [10, 20, 30, 40, 50];
    let mut index = 0;

    while index < 5 {
        println!("the value is: {}", a[index]);

        index += 1;
    }
}
```
14) You can also use `for` loops too
```rust
fn main() {
    let a = [10, 20, 30, 40, 50];

    for element in a {
        println!("the value is: {element}");
    }
}
```
```rust
fn main() {
    for number in (1..4).rev() { // .rev() reverses it
        println!("{number}!");
    }
    println!("LIFTOFF!!!");
}
```
