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

3. 🌟
```rust
// 填空
fn main() {
    let mut s = String::new();
    s.push_str("hello, world");
    s.push('!');

    assert_eq!(s, "hello, world!");
}
```

4. 🌟🌟🌟
```rust
// 修复所有错误，并且不要新增代码行
fn main() {
    let mut s = String::from("hello");
    s.push(',');
    s.push_str(" world");
    s += "!";

    println!("{}", s)
}
```

5. 🌟🌟 我们可以用 replace 方法来替换指定的子字符串
```rust
// 填空
fn main() {
    let s = String::from("I like dogs");
    // 以下方法会重新分配一块内存空间，然后将修改后的字符串存在这里
    let s1 = s.replace("dogs", "cats");

    assert_eq!(s1, "I like cats")
}
```

6. 🌟🌟 你只能将 String 跟 &str 类型进行拼接，并且 String 的所有权在此过程中会被 move
```rust
// 修复所有错误，不要删除任何一行代码
fn main() {
    let s1 = String::from("hello,");
    let s2 = String::from("world!");
    let s3 = s1.clone() + &s2; 
    assert_eq!(s3,"hello,world!");
    println!("{}",s1);
}
```
