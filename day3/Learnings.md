# Day 3
1) There are two main data type subsets. They are: scalar and compound.
2) We must add type annotation to variables whenever possible.
3) Scalar type represents a single value. There are 4 types of scalar value:
    a) integers b) floating-point numbers c) Booleans d) characters.
4) Check the types
- 8-bit: signed: i8, unsigned: u8
- 16-bit: signed: i16, unsigned: u16
- 32-bit: signed: i32, unsigned: u32
- 64-bit: signed: i64, unsigned: u64
- 128-bit: signed: i128, unsigned: u128
- arch: signed: isize, unsigned: usize

	Signed range: -(2^(n-1)) to 2^(n-1) where n is the bit size <br/>
	Unsigned range: 0 to 2^(n-1) <br/>
	The default is i32 tho.
5) Floating-points are of two types only:
    a) f32 b) f64 (default)
6) Rust allows all basic mathematical calc:
```rust
fn main() {
    // addition
    let sum = 5 + 10;

    // subtraction
    let difference = 95.5 - 4.3;

    // multiplication
    let product = 4 * 30;

    // division
    let quotient = 56.7 / 32.2;
    let truncated = -5 / 3; // Results in -1

    // remainder
    let remainder = 43 % 5;
}
```

Compound types are:-
1) Tuple type:-
- cannot shrink or grow in size
```rust
fn main() {
    let tup: (i32, f64, u8) = (500, 2.1, 3);
}
```
to acess these variables we can do something like this:-
```rust
    let (x, y, z) = tup;
    // OR
    let five_hunnid = tup.0;
```

2) Array type:-
- supports only one type, cannot shrink or grow in size
```rust
    let arr: [i32, 5] = [1,2,3,4,5];
    // or we can do
    let arr: [3, 5]; // this will fill arr with the number 3 for upto 5 times
```
