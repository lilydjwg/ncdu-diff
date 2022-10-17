ncdu fork that can compare and diff results

## NOTICE

Please use [gdu](https://github.com/dundee/gdu) (which doesn't need to be patched) and [gdu-diff](https://github.com/lilydjwg/gdu-diff) to accomplish the same tasks.

## Compile and Install

```sh
autoreconf -i
./configure
make
make install
```

Copy `ncdu-diff` and `ncdu-diffdir` somewhere (e.g. in your `$PATH`). You'll need Python to run them.

## Usage

Run:

```sh
ncdu-diffdir /directory/a /directory/b
```

Or you can do steps manually (and optionally save intermediate results.

Export two scan results:

```sh
ncdu -o old.ncdu /some/directory
ncdu -o new.ncdu /some/directory
```

Generate diff:
```sh
ncdu-diff old.ncdu new.ncdu > diff.ncdu
```

Load and view the diff:
```sh
ncdu -f diff.ncdu
```
