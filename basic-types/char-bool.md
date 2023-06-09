1. 🌟
```rust
// 修改2处 `assert_eq!` 让代码工作

use std::mem::size_of_val;
fn main() {
    let c1 = 'a';
    assert_eq!(size_of_val(&c1), 4); 

    let c2 = '中';
    assert_eq!(size_of_val(&c2), 4); 

    println!("Success!")
} 
```

2. 🌟
```rust
// 修改一行让代码正常打印
fn main() {
    let c1 = '中';
    print_char(c1);
} 

fn print_char(c : char) {
    println!("{}", c);
}
```
