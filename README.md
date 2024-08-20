This repo holds the e1000 driver [extracted from FreeBSD](https://github.com/freebsd/freebsd-src/tree/main/sys/dev/e1000).

## Updating from upstream

In a clone of the upstream FreeBSD repo, run:

```sh
git filter-repo --subdirectory-filter sys/dev/e1000/ --force
git filter-repo --path-regex 'e1000_osdep.[ch]' --invert-paths
git filter-repo --path-regex 'e1000_*' --path 'LICENSE'
```
