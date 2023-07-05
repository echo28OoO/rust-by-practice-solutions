1. 🌟 对于结构体，我们必须为其中的每一个字段都指定具体的值
```rust
// fix the error
struct Person {
    name: String,
    age: u8,
    hobby: String
}
fn main() {
    let age = 30;
    let p = Person {
        name: String::from("sunface"),
        age,
        hobby: String::from("kk"),
    };
} 
```

2. 🌟 单元结构体没有任何字段。
```rust

struct Unit;
trait SomeTrait {
    // ...定义一些行为
}

// 我们并不关心结构体中有什么数据( 字段 )，但我们关心它的行为。
// 因此这里我们使用没有任何字段的单元结构体，然后为它实现一些行为
impl SomeTrait for Unit {  }
fn main() {
    let u = Unit;
    do_something_with_unit(u);
} 

// 填空，让代码工作
fn do_something_with_unit(u: Unit) {   }
```

3. 🌟🌟🌟 元组结构体看起来跟元组很像，但是它拥有一个结构体的名称，该名称可以赋予它一定的意义。由于它并不关心内部数据到底是什么名称，因此此时元组结构体就非常适合。
```rust
// 填空并修复错误
struct Color(i32, i32, i32);
struct Point(i32, i32, i32);
fn main() {
    let v = Color(0, 127, 255);
    check_color(v);
}   

fn check_color(p: Color) {
    let Color(x, _, _) = p;
    assert_eq!(x, 0);
    assert_eq!(p.1, 127);
    assert_eq!(p.2, 255);
 }
```
