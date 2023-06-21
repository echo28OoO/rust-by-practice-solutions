1. 🌟 正常情况下我们无法使用 str 类型，但是可以使用 &str 来替代
```rust
// 修复错误，不要新增代码行
fn main() {
    let s: &str = "hello, world";
}
```

2. 🌟🌟 如果要使用 str 类型，只能配合 Box。 & 可以用来将 Box<str> 转换为 &str 类型
```rust
// 使用至少两种方法来修复错误
fn main() {
    let s: Box<str> = "hello, world".into();
    greetings(&s)
}

fn greetings(s: &str) {
    println!("{}",s)
}

// 使用至少两种方法来修复错误
fn main() {
    let s: Box<str> = "hello, world".into();
    greetings(s)
}

fn greetings(s: Box<str>) {
    println!("{}",s)
}

// 使用至少两种方法来修复错误
fn main() {
    let s: Box<&str> = "hello, world".into();
    greetings(*s)
}

fn greetings(s: &str) {
    println!("{}",s)
}
```
