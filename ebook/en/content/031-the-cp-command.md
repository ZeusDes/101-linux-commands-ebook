# The `cp` command

The `cp` is a command-line utility for copying files and directory.
cp stands for copy. This command is used to copy files or group of files or directory. It creates an exact image of a file on a disk with different file name. cp command require at least two filenames in its arguments.

### Examples:

1. To copy the contents of the source file to the destination file.

```
cp sourceFile destFile
```

If the destination file doesnt exists then the file is created and then the content is copied to it. If it exists then the file is overwritten. 2. To copy a file to another directory
Specify the absolute or the relative path to the destination directory.

```
cp sourceFile /folderName/destFile
```

3. To copy a directory, including all its files and subdirectories

```
cp -R folderName1 folderName2
```

The command above creates the destination directory and recursively copy all files and subdirectories from the source to the destination directory.

If the destination directory already exists, the source directory itself and its content are copied inside the destination directory.

4. To copy only the files and subdirectories but not the source directory

```
cp -RT folderName1 folderName2
```

### Syntax:

The general syntax for the cp command is as follows:

`cp [OPTIONS] SOURCE... DESTINATION`

The SOURCE can contain one or more files or directories as arguments, and the DESTINATION argument can be a single file or directory.

#### Some useful options

1. `-i` (interactive)
   `i` stands for Interactive copying. With this option system first warns the user before overwriting the destination file. cp prompts for a response, if you press y then it overwrites the file and with any other option leave it uncopied.

```
$ cp -i file1.txt fileName2.txt
cp: overwrite 'file2.txt'? y
```

2. `-b`(backup)
   -b(backup): With this option cp command creates the backup of the destination file in the same folder with the different name and in different format.

```
$ ls
a.txt b.txt

$ cp -b a.txt b.txt

$ ls
a.txt b.txt b.txt~
```

3. `-f`(force)
   If the system is unable to open destination file for writing operation because the user doesn’t have writing permission for this file then by using -f option with cp command, destination file is deleted first and then copying of content is done from source to destination file.
```
$ ls -l b.txt
-r-xr-xr-x+ 1 User User 3 Nov 24 08:45 b.txt
```
User, group and others doesn't have writing permission.

Without `-f` option, command not executed

```
$ cp a.txt b.txt
cp: cannot create regular file 'b.txt': Permission denied
```

With -f option, command executed successfully
```
$ cp -f a.txt b.txt
```
