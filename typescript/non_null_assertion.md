# non-null assertion

在變數後面多一個`!`就能讓變數類型從 ` T| undefined` 變成 `T` 直接使用就是快速表示這變數不會是空的

```ts
const a: string|null = "test"
a // string|null
a! // string
```
