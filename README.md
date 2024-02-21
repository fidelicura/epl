# Description

Insipiring humanity with simple, explicit and readable code!

# Features

- Interoperability: **C** language (_full_);
- Types: **strong**, **static**, **structural-algebraic**, **postfix-manifest**;
- Metaprogramming: **reflective** (_via compile-time metadata_), **CTFE** with **type of all types**;
- Memory: **explicit allocators**, **immutability by default**;
- Namespace: **first-class modules** (_compile-time_);
- Design: **data-oriented**;
- Runtime: **no**;

# Example

### Variables and pointers

```rust
// immutable and mutable variables
let some_variable: u8;
mut another_variable: u32;

// sized and unsized arrays
let some_sized_arr: [f32; 12];
mut some_unsized_arr: [i16];
```

### Branching

```rust
// match clause (variable is not a bool type)
match (variable) {
    variant_1: expr,
    // recall mechanism (switch like motion)
    variant_2: {
        expr;
        recall;
    },
}

// if-else alternative in match (if is_color is bool type)
match (is_color) {
    print("Colored!");
} else (is_enough_light) {
    print("Not enough light to determine color!");
} else {
    print("Not colored!");
}
```

### Functions

```rust
@inline
pub fn sum(first: *i32, second: i32) i32 {
    // in-place pointer dereferencing
    return *first + second;
}

@no_checks+no_mangle+linux
// fn add(mut* mut i32 first, i32 second) ErrorName:void {
fn add(first: mut*i32, second: i32) ErrorName:void {
    // "black box" clause
    // basically saying to the compiler "don't optimize this"
    persistent {
        // will increase pointer destination address, not a value after the ptr
        first += second;
    }
}

@windows
pub fn weird(first: fn, second: fn) i32 // named anonymous functions
    where
        first(i32) i32, // annotation by upper function prototype
        second() i32,
{
    return first(second());
}
```

### Loops

```rust
// while-loop alternative (is_night is bool)
loop (is_night) {}

// for-loop alternative (auto array indexing by ctx)
loop (|val: i32, idx: u8| arr, 0..) {}

// infinite loop
loop {}
```

### Composables

```rust
// structs with persistent fields
// and implemented methods
struct Point {
    let x: i32;
    var y: i32;

    persistent {
        mut amount: i32 = 0,
    }

    pub fn new(x: i32, y: i32) Self {
        Self { x, y }
    }
};

// simple C-like union
union Value {
    // WIP: tags (optional)
    tag

    var float: f32;
    var integer: i32;
    let byte: u8;

    // WIP: parametric polymorphism generics bound auto inference
    // compiler will automagically infer bounds
    // for generic by possible types of this union
    pub fn new(any value) Self {
        Self { value }
    }
};

// enum
pub enum Value {
    Float(f32);
    Integer(i32, i32);
    Byte;

    fn nothing() {}
};
```

### Modules

```rust
```

### Attributes

```rust
// attribute (WIP)
pub attr inline {}
```

### Metaprogramming

```rust
```

# Additionals

- First compiler written in OCaml;
- Compiler bootstrapping is one of the goals;
