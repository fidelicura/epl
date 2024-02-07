# Description

Insipiring humanity with simple, explicit and readable code!

# Features

- Interoperability: **C** language (_full_);
- Type system: **strong**, **static**, **structural-algebraic**, **manifest**;
- Metaprogramming: **reflective** (_via compile-time metadata_);
- Memory: **explicit allocators**, **immutability by default**;
- Namespace: **first-class modules**;
- X;

# Example

### Variables and pointers

```rust
// immutable and mutable variables
u8 some_variable;
mut i32 another_variable;

// sized and unsized arrays
[f32; 12] some_sized_arr;
[i16] some_unsized_arr;
```

### Branching

```rust
// match clause
match (variable) {
    variant_1: expr,
    // recall mechanism (switch motions)
    variant_2: {
        expr;
        recall;
    },
}

// if-else alternative in match
match (is_color) {
    print("Colored!");
} else match (is_enough_light) {
    print("Not enough light to determine color!");
} else {
    print("Not colored!");
}
```

### Functions

```rust
@inline
pub fn sum(*mut i32 first, i32 second) i32 {
    // in-place pointer dereferencing
    return *first + second;
}

@no_checks+no_mangle+linux
fn add(mut* mut i32 first, i32 second) ErrorName:void {
    // "black box" clause
    // basically saying to the compiler "don't optimize this"
    persistent {
        first += second;
    }
}

@windows
pub fn weird(fn first, fn second) i32
    where
        first(i32) i32,
        second() i32,
{
    return first(second());
}
```

### Loops

```rust
// while-loop alternative
loop (is_night) {}

// for-loop alternative
loop (i32 val, i32 idx: arr, 0..) {}

// infinite loop
loop {}
```

### Composables

```rust
// structs with persistent fields
// and implemented methods
struct Point {
    i32 x;
    i32 y;

    persistent {
        mut i32 amount = 0,
    }

    pub fn new(i32 x, i32 y) Self {
        Self { x, y }
    }
};

// simple C-like union
union Value {
    // WIP: tags (optional)
    tag

    f32 float;
    i32 integer;
    u8 byte;

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
