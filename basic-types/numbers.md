1. 🌟
```rust
// 移除某个部分让代码工作
fn main() {
    let x: i32 = 5;
    let mut y = 5;

    y = x;
    
    let z = 10; // 这里 z 的类型是?  i32
}
```

2. 🌟
```rust
// 填空
fn main() {
    let v: u16 = 38_u8 as u16;
}
```

3. 🌟🌟🌟
```rust
// 修改 `assert_eq!` 让代码工作
fn main() {
    let x = 5;
    assert_eq!("i32".to_string(), type_of(&x));
}

// 以下函数可以获取传入参数的类型，并返回类型的字符串形式，例如  "i8", "u8", "i32", "u32"
fn type_of<T>(_: &T) -> String {
    format!("{}", std::any::type_name::<T>())
}
```

4. 🌟🌟
```rust
// 填空，让代码工作
fn main() {
    assert_eq!(i8::MAX, 127); 
    assert_eq!(u8::MAX, 255); 
}
```

5. 🌟🌟
```rust
// 解决代码中的错误和 `panic`
fn main() {
   let v1 = 231_u8 + 8;
   let v2 = i8::checked_add(119, 8).unwrap();
   println!("{},{}",v1,v2);
}
```

6. 🌟🌟
```rust
// 修改 `assert!` 让代码工作
fn main() {
    let v = 1_024 + 0xff + 0o77 + 0b1111_1111;
    assert!(v == 1597);
}
```

