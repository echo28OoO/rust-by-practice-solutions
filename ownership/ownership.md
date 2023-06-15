1. 🌟🌟
```rust

fn main() {
    // 使用尽可能多的方法来通过编译
    let x = String::from("hello, world");
    let y = &x;
    println!("{},{}",x,y);
}


fn main() {
    // 使用尽可能多的方法来通过编译
    let x = "hello, world";
    let y = x;
    println!("{},{}",x,y);
}

fn main() {
    let x = &String::from("hello, world");
    let y = x;
    println!("{},{}",x,y);
}

fn main() {
    let x = String::from("hello, world");
    let y = x.as_str();
    println!("{},{}",x,y);
}
```

2. 🌟🌟
```rust
// 不要修改 main 中的代码
fn main() {
    let s1 = String::from("hello, world");
    let s2 = take_ownership(s1);

    println!("{}", s2);
}

// 只能修改下面的代码!
fn take_ownership(s: String) -> String {
    println!("{}", s);
    s
}
```

3. 🌟🌟
```rust

fn main() {
    let s = give_ownership();
    println!("{}", s);
}

// 只能修改下面的代码!
fn give_ownership() -> String {
    let s = String::from("hello, world");
    // convert String to Vec
    // 将 String 转换成 Vec 类型
    let _s = s.as_bytes();
    s
}
```

4. 🌟🌟
```rust
// 修复错误，不要删除任何代码行
fn main() {
    let s = String::from("hello, world");

    print_str(&s);

    println!("{}", s);
}

fn print_str(s: &String)  {
    println!("{}",s);
}

// 修复错误，不要删除任何代码行
fn main() {
    let s = String::from("hello, world");

    print_str(s.clone());

    println!("{}", s);
}

fn print_str(s: String)  {
    println!("{}",s);
}
```
