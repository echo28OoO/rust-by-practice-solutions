1. 🌟 变量只有在初始化后才能被使用
```rust
// 修复下面代码的错误并尽可能少的修改
fn main() {
    let x: i32 = 1; // 未初始化，但被使用
    let y: i32; // 未初始化，也未被使用
    println!("x is equal to {}", x); 
}
```

2. 🌟🌟 可以使用 mut 将变量标记为可变
```rust
// 完形填空，让代码编译
fn main() {
    let mut x = 1;
    x += 2; 
    
    println!("x = {}", x); 
}
```

3. 🌟 作用域是一个变量在程序中能够保持合法的范围
```rust
// 修复下面代码的错误并使用尽可能少的改变
fn main() {
    let x: i32 = 10;
    let y: i32 = 5;
    {
        let y: i32 = 5;
        println!("x 的值是 {}, y 的值是 {}", x, y);
    }
    println!("x 的值是 {}, y 的值是 {}", x, y); 
}
```

4. 🌟🌟
```rust
// 修复错误
fn main() {
    define_x();
}

fn define_x() {
    let x = "hello";
    println!("{}, world", x); 
}
```

5. 🌟🌟 若后面的变量声明的名称和之前的变量相同，则我们说：第一个变量被第二个同名变量遮蔽了( shadowing )
```rust
// 只允许修改 `assert_eq!` 来让 `println!` 工作(在终端输出 `42`)
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 12);
    }

    assert_eq!(x, 5);

    let x = 42;
    println!("{}", x); // 输出 "42".
}
```
