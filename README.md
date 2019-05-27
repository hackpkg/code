# Code

Tool to help maintain a personal monorepo

## Monorepo Structure

Everything exists under the `CODEPATH` environment variable. For example, if the
`export CODEPATH = "~/code"`, then the code directory would look something like
this.

```
$HOME/code
    bin/
        hello                          # command executable
        outyet                         # command executable
    src/
        github.com/TerrenceHo/code/
            .git/                      # Git repository metadata
            <Code files> ...
        github.com/golang/go
```

## Usage

```
code get github.com/hackpkg/code
```

```
code update
```
Runs the command to update a repository from its remote source. 

```
code build
```
Runs a command(s) to build some output.

```
code install
```
Builds and installs the executable the $CODEPATH/bin directory.

## .CODEFILE

The .CODEFILE specifies what commands to run for updating, building, and
installing binaries will be. The format will look something like the TOML
format, an example below.

```toml
# CODEFILE

[core]
source = "github.com/hackpkg/code"
build = "make"
install = "make install"
```
