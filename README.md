# Code

Tool to help maintain a personal monorepo

## Monorepo Structure

Everything exists under the `CODEPATH` environment variable. 

```
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
code clone github.com/TerrenceHo/code
```


