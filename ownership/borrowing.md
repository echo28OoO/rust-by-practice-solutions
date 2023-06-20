1. 🌟
```rust
fn main() {
   let x = 5;
   // 填写空白处
   let p = &x;

   println!("x 的内存地址是 {:p}", p); // output: 0x16fa3ac84
}
```

2. 🌟
```rust
fn main() {
    let x = 5;
    let y = &x;

    // 只能修改以下行
    assert_eq!(5, *y);
}
```

3. 🌟
```rust
// 修复错误
fn main() {
    let mut s = String::from("hello, ");

    borrow_object(&s)
}

fn borrow_object(s: &String) {}
```
