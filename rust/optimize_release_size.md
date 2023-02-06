# 優化rust build --release 目標的大小

參考於 ![johnthagen/min-sized-rust](https://github.com/johnthagen/min-sized-rust)

```toml
[profile.release]
opt-level = "z"  # Optimize for size.
lto = true
codegen-units = 1
panic = 'abort'
```

最後可以使用upx進行優化 但產出的目標可能會被防毒軟體誤判為有毒!

`upx --best --lzma target/release/xxx`
