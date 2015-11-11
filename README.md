[![npm](https://nodei.co/npm/cli-wd.png)](https://nodei.co/npm/cli-wd/)

# cli-wd [![Dependency Status][david-badge]][david]

[david]: https://david-dm.org/eush77/cli-wd
[david-badge]: https://david-dm.org/eush77/cli-wd.png

Run program in a modified working directory.

## Example

```
$ wd /usr/bin pwd
/usr/bin
```

Put archive file in a custom directory across archivers:

```
$ wd ./dir tar cvaf ../dir.tbz2 .
$ wd ./dir zip -r ../dir .
$ wd ./dir 7z a ../dir . -tzip
```

Start a subshell:

```
$ wd /
$ echo $SHLVL $PWD
2 /
```

## CLI

```
Usage:  wd <directory> [<command>] [arg]...
```

Run `<command>` (which defaults to `$SHELL`) with supplied arguments in a given working directory. Fall back to shell (just in case `<command>` is a shell function or alias).

## Install

```shell
npm install -g cli-wd
```

## License

MIT
