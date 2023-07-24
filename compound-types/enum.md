1. 🌟🌟 在创建枚举时，你可以使用显式的整数设定枚举成员的值。
```rust
// 修复错误
enum Number {
    Zero,
    One,
    Two,
}

enum Number1 {
    Zero = 0,
    One,
    Two,
}

// C语言风格的枚举定义
enum Number2 {
    Zero = 0,
    One = 1,
    Two = 2,
}


fn main() {
    // 通过 `as` 可以将枚举值强转为整数类型
    assert_eq!(Number::One as u8, Number1::One as u8);
    assert_eq!(Number1::One as u8, Number2::One as u8);
} 
```

2. 🌟 枚举成员可以持有各种类型的值
```rust

// 填空
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    Write(String),
    ChangeColor(i32, i32, i32),
}

fn main() {
    let msg1 = Message::Move{x: 1, y: 2}; // 使用x = 1, y = 2 来初始化
    let msg2 = Message::Write(String::from("hello, world!")); // 使用 "hello, world!" 来初始化
} 
```

3. 🌟🌟 枚举成员中的值可以使用模式匹配来获取
```rust

// 仅填空并修复错误
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    Write(String),
    ChangeColor(i32, i32, i32),
}

fn main() {
    let msg = Message::Move{x: 1, y: 1};

    if let Message::Move{x: a, y: b} = msg {
        assert_eq!(a, b);
    } else {
        panic!("不要让这行代码运行！");
    }
} 
```
