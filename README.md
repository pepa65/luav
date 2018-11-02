# luavm - Lua Version Manager

**Command line tool to manage and switch between different versions of `lua`,
`LuaJIT` and `luarocks`.**

## Features

1. Installs/Uninstalls any version of `lua`, `LuaJIT` or `luarocks`.
2. Switches between different versions of `lua`, `LuaJIT` or `luarocks`.
3. Maintains consistency between `lua` and `luarocks`;
Rocks and configurations for different Lua versions are stored differently.

## Requirements

**`wget` `make` `libreadline-dev`
`lib32ncurses5-dev`**: for 32-bit (earlier) versions of Lua on 64 bit machines.
**`liblua5.3-dev` `liblua5.2-dev` `liblua5.1.0-dev` `liblua50-dev`**, depending
on the Lua version used for compiling `LuaJIT`.

## Installation

```sh
wget -qO- https://gitlab.com/pepa65/luavm/raw/master/luavm-install |bash
```

## Usage
### Sample usage:

```sh
luavm install 5.3.5             # Installs latest lua-5.3
luavm install 5.2.4             # Installs latest lua-5.2
luavm install 5.1.5             # Installs latest lua-5.1
luavm install 5.0.3             # Installs latest lua-5.0
luavm install-luarocks 3.0.4    # Installs latest version
luavm install-luajit 2.0.3      # Installs latest luajit version
```

### Complete usage:

```sh
Usage:  luavm [help] | list[-{luajit|luarocks} | current | version |
          {install|use|uninstall}[-{luajit|luarocks}] <version>

  luavm [help]                          Display this message
  luavm install <version>               Install lua-<version>
  luavm use <version>                   Use lua-<version>
  luavm uninstall <version>             Uninstall lua-<version>
  luavm list                            List installed lua versions
  luavm install-luajit <version>        Install LuaJIT-<version>
  luavm use-luajit <version>            Use LuaJIT-<version>
  luavm uninstall-luajit <version>      Uninstall LuaJIT-<version>
  luavm list-luajit                     List installed LuaJIT versions
  luavm install-luarocks <version>      Install luarocks<version>
  luavm use-luarocks <version>          Use luarocks-<version>
  luavm uninstall-luarocks <version>    Uninstall luarocks-<version>
  luavm list-luarocks                   List installed luarocks versions
  luavm current                         List current versions being used
  luavm version                         Display luavm version
```

## Contribution

Feel free to [file issues](https://gitlab.com/pepa65/luavm/issues).

## License

luavm is licensed under the [MIT license](http://dhaval.mit-license.org/),
relicenced under GPL3+ (c) 2018 pepa65@passchier.net
