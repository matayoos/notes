# Ubuntu learning

### Links

- Symbolic links: it's like a system variable...
	* *ln -s item link*

- Hard links: unlike a symbolic link, when we list a directory containing a hard link we **will see no special indication of the link**. When a hard link is deleted, the link is removed but the contents of the file itself continue to exist (**that is, its space is not deallocated**)
	* *ln file link*

### Wildcars

```bash
- *	All files
- g*	Any files begginning with "g"
- b*.txt	Any files beggining with "b" followed for any characters and ending with ".txt"
- [[:upper:]]*	Any file beggining with an uppercase letter
- And many else
```

### Copy

```bash
- cp item... directory
- cp -i
	* cp assuming you know what we know we're doing. To get a warning, we'll include the  "-i" (interactive) option.
- cp file1 file 2 dir1	Copy file1 and file2 into directory dir1. The directory dir1 must already exists.
```

- The command *mv* works similar

###
