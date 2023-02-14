# rust交叉編譯

`rustup target add <target>`

可以使用這指令增加編譯目標，他會下載該目標的編譯工具
需要注意的是不同目標可能有不同的系統需求或依賴需要先安裝

`cargo build --target <targer>`

之後就可以用`cargo`來編譯該目標的binary

目標列表在這邊參考: https://rust-lang.github.io/rustup/installation/index.html
