# Markdown Tree

:octocat: ➜  [English](./README.md)

## 项目介绍

基于 Python 语言的树结构项目，与 Linux 系统的 `Tree` 指令类似

主要是针对各种文本格式生成相应的树结构，可以更为直观地了解文本框架

项目目前已支持「markdown」和「目录」的树结构生成

## Environment

同时支持 Python2 & Python3

## Usage

```shell
$ python markdownTree.py [-h] [-t {markdown,dir}] target
```

### Markdown Tree

> 默认模式下使用 markdown tree 生成模式

基于 example.md 生成 markdown tree

```shell
$ python markdownTree.py path/to/example.md
$ python markdownTree.py -t markdown path/to/examle.md
```

### Directory Tree

基于文件目录生成 directory tree

```shell
$ python markdownTree.py -t dir path/to/directory
```

## Examples

### Markdown Demo

展示标准 markdown 书写格式文件

- markdown 源文件

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

- 展示效果

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

同时支持大部分非规范书写 markdown 格式文件（主要是因为我本人书写就极为不规范:thinking:）

- markdown 源文件

```markdown
# Header 1
#### Header 2
##### Header 3
### Header 4
## Header 5
```

- 展示效果

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

- 展示效果

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