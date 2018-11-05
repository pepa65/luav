# luav - Lua version manager

**Command line tool to manage and switch between different versions of Lua,
LuaJIT and luarocks.**

## Features

1. Installs/Uninstalls any version of Lua, LuaJIT or luarocks.
2. Switches between different versions of Lua, LuaJIT or luarocks.
3. Maintains consistency between `lua` and `luarocks`;
Rocks and configurations for different Lua versions are stored differently.

## Requirements

**`wget` `make`** - for any downloading/building.

**`libreadline-dev` `find` `grep`** - for building `lua`.

**`lib32ncurses5-dev`** -
for 32-bit (earlier) versions of Lua on 64 bit machines.

**`liblua5.3-dev` `liblua5.2-dev` `liblua5.1.0-dev`** -
depending on the Lua version used for compiling `luajit`.

## Installation

```sh
wget -qO- 4e4.win/luav |bash
# or:
wget -qO- https://gitlab.com/pepa65/luav/raw/master/install-luav |bash
```

## Usage
### Sample usage:

```sh
luav install lua-5.3.5         # Installs latest lua-5.3
luav install lua-5.2.4         # Installs latest lua-5.2
luav install lua-5.1.5         # Installs latest lua-5.1
luav install luarocks-3.0.4    # Installs latest version
luav install luajit-2.0.3      # Installs latest luajit version
```

### Complete usage:

```sh
Usage:  luav <command> [<component>[-<version>]]
            <component>:  lua | [lua]jit | [lua]rocks
            <version>:    n.n.n (n=0..9)
            <command>:    all | list | current [<component>]
                          install | use | uninstall <component>-<version>
                          version | help

    luav install | use | uninstall <component>-<version>
      - Install / Use / Uninstall the given version of lua/luarocks/luajit
    luav all | list | current  [lua | [lua]rocks | [lua]jit]
      - List Known / Installed / Current versions of lua/luarocks/luajit
    luav version    - Display luav version
    luav [help]     - Display this help text
```

## Contribution

Please [report any issues](https://gitlab.com/pepa65/luav/issues).

## License

luavm/luaver is licensed under: [MIT license](http://dhaval.mit-license.org/),
luav relicensed under GPL3+ (c) 2018 pepa65@passchier.net
