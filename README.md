# QEMU notes
## Table of Contents
[[_TOC_]]

## Description 

Sometimes remembering exact syntax or options of a command or tool. 
This is an effort to compile that information into central repository. For example:  
- You know that `find` can execute commmands on found files, but forgot the syntax?  
Was it `-exec <command> {};` or `-exec <command> {}\;`?  
Was there a space?  
- Or that handy `rsync` option?
- How did I suppose to redirect both output and error into?  
`2&1>` or `2>&1`?

## Find
### Execute a command on found files 
```bash
find . -type f -[i]name '*.txt' -exec grep -q 'hello' {} ';'
```
`-type <letter>`. `letter` can be:
- `b` -> block
- `f` -> regular file
- `d` -> directory
- `l` -> symbolic link

`-name <pattern>` -> file name(not directory) in shell patern format to match  
`-iname` -> insensitive `name`

`-exec <command> [{}] ';|+'`
### References
- https://unix.stackexchange.com/questions/389705/understanding-the-exec-option-of-find/389706#389706

## Pacman
### Find files installed by a package
```bash
$ pacman -Ql pacman|grep /usr/bin/
pacman /usr/bin/makepkg
pacman /usr/bin/makepkg-template
pacman /usr/bin/pacman
pacman /usr/bin/pacman-conf
pacman /usr/bin/pacman-db-upgrade
pacman /usr/bin/pacman-key
pacman /usr/bin/repo-add
pacman /usr/bin/repo-elephant
pacman /usr/bin/repo-remove
pacman /usr/bin/testpkg
pacman /usr/bin/vercmp
```

## Awk

## Sed

## Vim

## Grep

## Lxc

## Docker

## Ansible

## Qemu

## References
- 
