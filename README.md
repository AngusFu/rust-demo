# rust-demo

跟着 [The Rust Programming Language](https://doc.rust-lang.org/book/2018-edition) 敲代码。

> 下面记录了从安装 rust 环境到配置常用工具的步骤 ——

## 安装 rust

执行 [rustup.rs](https://rustup.rs/) 提供的命令即可。速度可能比较慢，似乎可以通过[使用中科大的源来解决](https://blog.csdn.net/xiangxianghehe/article/details/53471936)，不过不知为何我却失败了。最后我的解决方法是在家直接通过 VPN 连到公司的网络（公司网络好评）。

```
curl https://sh.rustup.rs -sSf | sh
```

## 安装 wasm-pack

因为我学习 rust 的最初动力是 WebAssembly，所以肯定要安装相关的工具。具体参见文档: [rustwasm.github.io/book](https://rustwasm.github.io/book/)

## 安装各种 cargo 工具

### cargo generate

用来快速生成模板项目的工具。

```
cargo install cargo-generate
```

使用示例：

```
cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

### cargo watch

主要用来监听文件变化。文档地址：[github.com/passcod/cargo-watch](https://github.com/passcod/cargo-watch)

```
cargo install cargo-watch
```

文档中的使用示例：

```
# Run run with arguments
$ cargo watch -x 'run -- --some-arg'
```

### 依赖管理

作为习惯了 `npm` 的前端党，怎么能受得了手写依赖这种事。可惜 `cargo install` 和 `npm install` 完全是两种行事风格。

最后找到了 [cargo-edit](https://github.com/killercup/cargo-edit)，可以说非常方便了。

```
cargo install cargo-edit
```

cargo-edit 提供了以下三个命令：

```
cargo add
cargo rm
cargo upgrade
```

## 其他：国内加速、docker 

SEE https://github.com/Brooooooklyn/sourcemap-decoder/blob/master/README.md

