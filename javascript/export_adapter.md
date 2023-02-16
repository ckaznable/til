# 能適應各種環境的適配器寫法

從 [Shopify/shopify-api-js](https://github.com/Shopify/shopify-api-js) 學習到
藉由替換掉已經export的方法來達到適配各種環境的寫法

adapter.ts
```ts
export let fetch = () => {
  throw new Error("needs impl fetch")
}

export function setFetch(fn: () => void) {
  fetch = fn
}
```

node.ts
```ts
import { setFetch } from "./adapter.ts"

setFetch(() => {
   // impl for nodejs
})
```

browser.ts
```ts
import { setFetch } from "./adapter.ts"

setFetch(() => {
   // impl for browser
})
```

之後只要在特定環境去import環境的檔案就可以

在nodejs
`import "node.ts"`

在瀏覽器
`import "browser.ts"`

