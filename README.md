# Markdown Tree

:octocat: ➜  [中文文档](./README_CN.md)

## Overview

A Python Tree Project.

Generate tree data structure of different type, like Linux `tree` command.

This project has already supported for markdown, directory up to now. 

## Environment

Support for both Python2 & Python3

## Usage

```shell
$ python markdownTree.py [-h] [-t {markdown,dir}] target
```

### Markdown Tree

> Default tree type is markdown tree.

generate markdown tree based on example.md

```shell
$ python markdownTree.py path/to/example.md
$ python markdownTree.py -t markdown path/to/examle.md
```

### Directory Tree

generate dirtory tree based on a directory

```shell
$ python markdownTree.py -t dir path/to/directory
```

## Examples

### Markdown Demo

Display standard markdown document.

- Source markdown document

```markdown
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
## Header 2a
### Header 3a
## Header 2a
```

- Effect

```shell
$ python markdownTree.py example.md
Header 1
├───Header 2
│   └───Header 3
│       └───Header 4
│           └───Header 5
├───Header 2a
│   └───Header 3a
└───Header 2a
```

Also adapted for most of documents that not follow standard writing rules. Caz author has made a lot of them already.​ :laughing:

- Source markdown document

```markdown
# Header 1
#### Header 2
##### Header 3
### Header 4
## Header 5
```

- Effect

```shell
$ python markdownTree.py example.md
Header 1
├───┐
│   ├───┐
│   │   └───Header 2
│   │       └───Header 3
│   └───Header 4
└───Header 5
```

### Directory Demo

- Effect

```shell
$ python markdownTree.py -t dir example
example
├── example1.md
├── example2.md
├── example3.md
├── note
│   ├── example4.md
│   └── example5.md
└── notedir
    ├── example6.md
    └── example7.md

2 directories, 7 files
```



## References

> Develop based on Project: https://github.com/kddeisz/tree