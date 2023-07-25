1. 🌟
```rust

// 填空
fn main() {
    let n = 5;

    if n < 0 {
        println!("{} is negative", n);
    } else if n > 0 {
        println!("{} is positive", n);
    } else {
        println!("{} is zero", n);
    }
} 
```

2. 🌟🌟 if/else 可以用作表达式来进行赋值
```rust

// 修复错误
fn main() {
    let n = 5;

    let big_n =
        if n < 10 && n > -10 {
            println!(" 数字太小，先增加 10 倍再说");

            10 * n
        } else {
            println!("数字太大，我们得让它减半");

            n / 2 
        };

    println!("{} -> {}", n, big_n);
} 
```

3. 🌟 for in 可以用于迭代一个迭代器，例如序列 a..b.
```rust

fn main() {
    for n in 1..100 { // 修改此行，让代码工作
        if n == 100 {
            panic!("NEVER LET THIS RUN")
        }
    }
} 
```

4. 🌟🌟
```rust

// 修复错误，不要新增或删除代码行
fn main() {
    let names = [String::from("liming"),String::from("hanmeimei")];
    for _name in &names {
        // do something with name...
    }

    println!("{:?}", names);

    let numbers = [1, 2, 3];
    // numbers中的元素实现了 Copy，因此无需转移所有权
    for _n in numbers {
        // do something with name...
    }
    
    println!("{:?}", numbers);
} 
```

5. 🌟
```rust
fn main() {
    let a = [4,3,2,1];

    // 通过索引和值的方式迭代数组 `a` 
    for (i,v) in a.iter().enumerate() {
        println!("第{}个元素是{}",i+1,v);
    }
}
```
