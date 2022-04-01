# Project Template for a Scopes Lang Library

This is a project template generator and updater using the
[copier](https://github.com/copier-org/copier/) tool for creating libraries for the [Scopes](http://scopes.rocks) programming language.

Please install from the latest copier for this to work, not the latest
stable release. Currently I am using
[pipx](https://github.com/pypa/pipx):

```sh
pipx install git+https://github.com/copier-org/copier.git@e98314063246993532048ba2ecf80a049154d2f6
```


## Generating a Project

Then you can generate your project:

```sh
copier 'gh:salotz/scopes-lib_copier-template' ./
```

This should generate the following (`repo_name = my-lib`):

```
my-lib
├── __env.sc
├── Makefile
├── README.md
├── spack.yaml
└── src
    └── my-lib
        ├── init.sc
        └── sanity.sc
```


## Development Environment

Create a [Spack](https://spack.io/) environment and install
dependencies

```
cd my-lib
spack env create -d .
spacktivate .
spack install
```

If you need more you can add them to `spack.yaml`.

Then you should be able to run the sanity check:

```sh
scopes -e -m my-lib.sanity
```

Start coding!


## Libraries Using this Template

- [scopes-raylib](https://github.com/salotz/raylib-scopes)
- [scopes-chipmunk2d](https://github.com/salotz/scopes-chipmunk2d)
