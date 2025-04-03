# Linux Commands

> Can also be used in MacOS terminal.

## mv

### rename multiple files extension

rename file extension from `.log` to `.txt`.

```shell
$ for i in *.log; do mv -- "$i" "${i%.log}.txt"; done
```

