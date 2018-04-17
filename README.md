_🇫🇷 Pour les instructions en français, veuillez consulter `LISEZMOI.md`_

## Installing Rust

### Standard procedure

At the time of writing, the easiest way is to use [rustup](https://www.rustup.rs/).

_Note: under Windows, you will have to choose between two options. For `gnu`, you need nothing special ; rustup will automatically install GNU compiler tools. For `msvc`, you need to install `Visual C++ Build Tools 2015` ; [click here for more details](https://github.com/rust-lang-nursery/rustup.rs/#user-content-vs2015)._

### Docker

If you don't want to install Rust on your local machine, you can use Docker: 

```bash
alias cargo='docker run --rm --tty --user $(id -u) --volume $(pwd):$(pwd) --workdir $(pwd) -e "USER=$(id -un)" loganmzz/rust cargo test'

cargo new foobar
cargo run
```

_Note: If you want a specific version, please consult available [image tags](https://hub.docker.com/r/loganmzz/rust/tags/). Also, remember to update latest with `docker pull loganmzz/rust`._

### Verification

To check your installation, just run `cargo run` from root directory of  repository [rust-workshop](https://github.com/loganmzz/rust-workshop). It should prints

```text
Congrulations !
You have compiled and run your first Rust program
```

## Installing editor

### [IntelliJ IDEA](https://www.jetbrains.com/idea/)

_Note: you can also use other IntelliJ-based products. But IntelliJ IDEA has a community version._

[IntelliJ Rust](https://intellij-rust.github.io/) is the official plug-ins. Firstly, started as side projects from JetBrains employees. Since summer 2017, it is officially supported by JetBrains.

### [Visual Studio Code](https://code.visualstudio.com/)

[Rust (rls)](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust) is currently the recommended extension. It is provided by Rust Developer Tools team (whih also provides [Rust Language Server](https://github.com/rust-lang-nursery/rls)).


There is also [Rust](https://marketplace.visualstudio.com/items?itemName=kalitaalexey.vscode-rust) but it's not actively developped. In this case, using RLS mode is highly recommanded.


### Others

You can find more supported IDEs at [Are we (I)DE yet?](https://areweideyet.com/).
