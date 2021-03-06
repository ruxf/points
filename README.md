# points
`rust` 中 使用 `fn` 来声明函数；而 `go` 语言中使用 `func`；`JavaScript` 中使用 `function`；`python` 中使用 `def`；`C` `C++` 中直接以返回值 `void` `int` `string` ... 来声明函数；

`rust` 中使用 `Vec` 来声明可变数组，是 `Vector` 的缩写；`C++` 中以 `Vector` 来生命可变数组；

`rust` 使用 `cfg!(debug_assertions)` 来条件编译 `debug` 模式下的输出；

`rust` `C` `C++` `Go` 语言中均使用 `"` 来代表字符串，使用单引号 `'` 来代表单个字符 `char`；在 `JavaScript` 中使用单引号 `'` 来代表字符串和单个字符 ；

`rust` 使用 `let` `var` 声明不可变变量， 使用 `let mut variable` 声明可变变量，`const` 声明常量；`Python` 中直接生命变量；`C` `C++` 中使用 `类型` + `variable` 来声明变量；`Go` 语言使用 `var` 声明变量；

`rust` 基本数据类型包括：
- 数值类型：有符号数值（`i8` `i16` `i32` `i64` `isize`），无符号数值（`u8` `u16` `u32` `u64` `usize`）
- 字符串：字符串字面量和切片 `&str`
- 布尔类型：`true` `false`
- 字符类型：单个 `char` Unicde类型存储为 `4` 个字节
- 单元类型：`()` 唯一的值也为 `()`

`rust` 使用 `panic` 抛出错误；`Go` 使用 `panic` 抛出错误；`Python` 使用 `raise` 抛出错误；`JavaScript` 使用 `throw` 抛出错误；

`rust` 中也包含有 `Nan`，使用 `is_nan` 来进行比较；

`rust` 中使用 `..` 来生成序列，[1, 5) 表示为 `1..5`，[1, 5] 表示为 `1..=5`；在 `Python` 中使用 `range` 函数来实现；

`rust` 中函数使用需要表明参数和返回值类型；无返回值时使用 `()` 表示，使用 `!` 表示函数永不返回；

`rust` 中使用 `"` 声明的字面量字符串是不可变的，如果需要声明动态字符串类型则需要使用 `String` 来实现；

`rust` 值所有权：
- 每一个值都有且只有一个所有者（变量）；
- 当所有者（变量）离开作用域范围后，该值将被丢弃（drop）；

`SheBang` 定义编译器属性：

- `#![allow(unused_variables)]` 允许未使用变量
- `#![allow(unused_doc_comments)]` 允许未使用的`comment`

使用 `rustc -W help` 查看 `rustc` 编辑器的 `Warn` `Allow` `Deny` `forbid` 规则；

`rust` 使用 `unimplemented!` 和 `todo!` 表示此处代码功能暂未实现；`Python` 中使用 `pass` 来表示此处功能暂未实现；

`rust` 中字符串有字面量类型 `&str` 和 动态字符串类型 `String`；

`rust` 中使用 `()` 声明元组类型；`Python` 中使用 `tuple` 来声明元组类型；`Go` 中使用 `Pair/Tuple` 来实现对和元组操作；

`rust` 中使用 `..` 来做序列分片或者解构；`JavaScript` 中使用 `...` 来做解构；

`struct` 没有实现 `Display` 特征，需要使用 `#[derive(Debug)]` 或者 `dbg!` 宏来打印 `struct`，同样可以自定义实现 `Display` 特征；

任何类型的数据都可以放入枚举成员中；

`Option` 确实是一个比较不错的设计，在 `JavaScript` 中比较混淆的就有 `undefined` 和 `null`，`undefined` 代表变量的值未定义，`null` 代表变量的值默认为空值；

在 `rust` 中有两种数组，一种是定长的 `array` 和动态长度的 `Vector` 动态数组；他们的关系就像 `&str` 和 `String` 一样；他们都属于 `rust` 的高级类型：`集合类型`；

`rust` 中的 `array` 是长度固定，大小固定的，因此属于 `基本类型`，存储在 `栈` 上；而 `Vector` 是不固定的，存储在 `堆` 上；

`rust` 中的 `if` `else if` 判断 `条件` 不需要添加 `()`;

`rust` 中的 `for` 循环，使用的是 `for in` 循环；`while` 循环需要将条件的变量声明为 `可变`；`loop` 循环需要搭配 `break` 使用；

`rust` 中使用 `match` 和 `if let` 进行模式匹配；`match` 和 `JavaScript` 中的 `switch case` 比较像，`match` 中的 `_` 默认值等同于 `switch case` 中的 `default`， `match` 中的 `=>` 等同于`case` 关键字后面的 `:`，另外一点是 `match` 的模式匹配中不需要添加 `break` 关键字结束匹配；模式匹配可以使用 `matchs!` 宏来进行简写；

`rust` 的 `Option<T>` 解构相当于使用三目运算符 `condition ? value : value` 来赋值；

`可驳模式匹配` 和 `不可驳模式匹配` 代表是否是全部匹配模式；

`rust` 中方法使用和 `Python` 中相同的参数名 `self` 代表当前结构体；

`rust` 中有一个约定成俗的规定使用 `new` 作为关联函数构造器的名称，处于设计上的考虑，`rust` 没有使用 `new` 作为关键字；

`rust` 中结构体的函数、枚举的值需要使用 `::` 来调用；`::` 用于模块和关联函数创建的命名空间；这一点和 `C++` 比较类似；

枚举类型不仅能 `统一化类型`， 并且能够像结构体一样实现方法；

我们可以为 `结构` `枚举` `特征` 实现方法；

`泛型` 和 `特征` 是 `rust` 中最最重要的抽象类型；

`TypeScript` 中设计的有 `泛型`；`rust` 中包含有 `泛型`； `Go` 语言最近支持了泛型开发；

`Option` 泛型枚举和 `Result` 泛型枚举是不可或缺的；

`rust` 中的特征 `trait` 相当于 `TypeScript` 中的接口 `interface`；

`特征` 定义了一个可以共享的行为，只要实现了该特征就可以使用该行为；

定义 `特征` 就是把一些方法组合在一起，目的是定义一个实现某些目标所必须的行为的集合；

使用 `trait` 关键字来定义特征；




 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY2NjIzMiwxNTg3NjY1MDA3LC0xOTA3OT
cyODM5LC04MDE1ODQ4MTMsNzQwNTMwMzAxLDE5MjI5MzM5Njks
MTkzMDU3NzA1MiwyMDU5NDYxNzUzLDUwNjkyMTEwLC0xNTk5OD
c3NDA2LDEyMTA3MDI1MTYsLTExNTk3MTk3NzgsLTExNzU3NzA1
NjYsLTM4MjMxOTg0OSwtMjUyMTc2NzkxLDEyODcxOTU0NDAsLT
EyMjU1MzczNTgsLTE2NzI5MDM2MzgsMTM5NDU2NjE5NywtMTg1
NjE1MjEzOF19
-->