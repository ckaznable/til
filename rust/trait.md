# `trait` 語法

以我的理解來說的話, `trait`比較像是其他語言的`interface`, 也就是一種約束, 但看起來只能約束方法名稱不能約束`struct`屬性

typescript:
```ts
interface A {
  getName() => string
}

class B implements A {
  getName() {
    return "test"
  }
}
```

rust:
```rs
trait A {
  fn get_name() -> String
}

struct B {}
impl A for B {
  fn get_name() -> String {
    String::from("test")
  }
}
```
