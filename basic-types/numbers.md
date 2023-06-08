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

7. 🌟
```rust
// 将 ? 替换成你的答案
fn main() {
    let x = 1_000.000_1; // f64
    let y: f32 = 0.12; // f32
    let z = 0.01_f64; // f64

    assert_eq!(type_of(&x), "f64".to_string());
    println!("Success!");
}

fn type_of<T>(_: &T) -> String {
    format!("{}", std::any::type_name::<T>())
}
```

8. 🌟🌟 使用两种方法来让下面代码工作
```rust
fn main() {
    assert!(0.1_f32 + 0.2_f32 == 0.3_f32);
}

fn main() {
    assert!((0.1_f64+ 0.2 - 0.3).abs() < 0.001);
}
```

9. 🌟🌟 两个目标: 1. 修改 assert! 让它工作 2. 让 println! 输出: 97 - 122
```rust
fn main() {
    let mut sum = 0;
    for i in -3..2 {
        sum += i
    }

    assert!(sum == -5);

    for c in 'a'..='z' {
        println!("{}",c as i32);
    }
}
```

10. 🌟🌟
```rust
// 填空
use std::ops::{Range, RangeInclusive};
fn main() {
    assert_eq!((1..5), Range{ start: 1, end: 5 });
    assert_eq!((1..=5), RangeInclusive::new(1, 5));
}
```

11. 🌟
```rust

