# CCPL for Visual Studio Code

[![Marketplace](https://img.shields.io/badge/marketplace-CCPL-53A0F5.svg)](https://marketplace.visualstudio.com/items?itemName=ccpl.ccpl)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.2.0-blue.svg)](CHANGELOG.md)

Syntax highlighting and editor support for **CCPL** â€” the *Cool Compilable Programming Language*, a Lua-like language that compiles straight to native executables through [TinyCC](https://bellard.org/tcc/).

> This repository contains **only the VS Code extension**. The language implementation lives in a separate repository.

## Features

- Syntax highlighting for `.ccpl` files
  - keywords and control flow (`if`/`elseif`/`else`, `while`, `repeat`/`until`, `for`, `return`, `break`, `continue`)
  - declarations (`var` / `variable`, `func`, `get`)
  - builtins (`say`, `hey`, `oh`, `tonumber`, `tostring`, `malloc`/`calloc`/`realloc`/`free`)
  - native types (`i8`â€¦`i64`, `u8`â€¦`u64`, `f32`, `f64`, `bool`, `char`, `ptr`)
  - numbers (decimal, float, exponent, hex), strings with escapes, operators
- Line comments (`--`) and block comments (`--[[ ... ]]`)
- Smart bracket and quote pairing
- A custom icon and dark gallery banner

## Install

### From the Marketplace

Search for **CCPL** in the VS Code Extensions view, or run:

```sh
code --install-extension ccpl.ccpl
```

### From a `.vsix`

```sh
code --install-extension ccpl-0.2.0.vsix
```

### From source

```sh
git clone https://github.com/itzdanti/vscode-ccpl.git
cd vscode-ccpl
npm install
npx vsce package
code --install-extension ccpl-0.2.0.vsix
```

## A taste of CCPL

```ccpl
-- hello world in CCPL
say("hello, world")

func add(a: i32, b: i32): i32
    return a + b
end

for i = 1, 3 do
    say("add", i, add(i, 10))
end
```

## Related repositories

| Project | Description | License |
| --- | --- | --- |
| **ccpl** | Compiler and language implementation | GPL-3.0 |
| **ccpl-toolchain** | Ready-to-run Windows toolchain bundle | GPL-3.0 |
| **vscode-ccpl** | This extension | MIT |

## Contributing

Issues and pull requests are welcome. Please open an issue before starting a larger change. To add highlighting, edit `syntaxes/ccpl.tmLanguage.json` and test with the `Developer: Inspect Editor Tokens and Scopes` command.

## License

Released under the [MIT License](LICENSE).
