## Some commands

### Print something to the terminal - echo
```
echo Hello!
```

### Print working directory - pwd
```
pwd
```

### Change directory - cd
```
cd directory-name
```

### List content - ls
```
ls
```
### Traversing the file system - cd
```
pwd
/Users/youruser/somefolder
cd ..
/Users/youruser
```
* using the ```..``` double period moves us back in our filesystem
```
pwd
/Users/youruser/somefolder
cd ../..
/Users
```
### Viewing file content - cat
```
cat filename.extension
```
* the `echo` command can also be used for viewing file content, but the `cat` command is more commonly used

#### Practice
- You could use the directory provided here or check items in your own computer
- If you are using windows, I would suggest trying to use WSL
```
house/
  ├── bathroom/
  │     └── medicine-cabinet/
  │           └── items.txt
  |── bedroom/
  │     └── closet/
  │           └── items.txt
  ├── dining-room/
  │     └── cabinet/
  |           └── items.txt
  ├── kitchen/
  │     ├── fridge/
  │     │     └── items.txt
  │     └── pantry/
  │           └── items.txt
  └── living-room/
        └── shelf/
              └── books.txt
```

### Clearing the command line - clear
```
clear
```

### Shortcuts

- keyboard's ↑ and ↓ arrow keys to navigate through previous commands
- tab for completing names of commands or existing files/directories

### Make directory - mkdir
```
mkdir new-directory-name
```

### Create New File - touch
```
touch filename.txt
```

### Write to a file 
- The command echo, prints out to the console, but it's possible to add content to a file
```
echo "Vintage tee, brand new phone" > cardigan.txt
```
- then you can even use the cat command to check the file content
```
cat cardigan.txt
```
- The ``>`` will overwrite any existing data, if we want to add content to a file, we use ``>>``
```
echo "High heels on cobblestone" >> cardigan.txt
```
### Combine Files
```
cat file-a > file-b
```
- The command above will pick up the information at file-a and overwrite file-b with it
```
cat chorus.txt >> cardigan.txt
```
- If we want to keep the content, like before, we use the ``>>``
```
$ cat cardigan
Vintage tee, brand new phone
High heels on cobblestone
And when I felt like I was an old cardigan
Under someone's bed
You put me on and said I was your favorite
```
### Move directories & files - mv
```
mv cardigan.txt albums/folklore/
```
### Renaming
```
mv albums discography
```
- the difference between moving is renaming is
- If the second argument of ``mv`` is neither a file nor a directory, the first argument is renamed to that

### Removing Directories & Files
- For files, we can use the ``rm`` command
```
rm exile.txt
```
- For removing directories, we can use the ``rmdir`` command
```
rmdir folklore/
```
- However the ``rmdir` command only removes empty directories
- To remove a non-empty directory, we'll need to use the ``rm`` command with a special ``-r`` flag
- ``-r`` stand for "recursively"
  
```
rm -r folklore
```
### Copy Files - cp
```
cp file-a file-b
```
- The copy will overwrite the file-b, if it exists, so it is similar to
- ``cat file-a > file-b``
- But it creates the file if it does not exists

### Copy Directories - cp -r
```
cp -r taylor-swift-playlist playlist-copy
```

### List everything under a directory
```
ls -R
```

## Cheat Sheet

|Command	| Description|
|---|---|
|echo output-here |	Print what is typed next to this command.|
|pwd	| Print the current working directory.|
|cat file-name.extension	| Print the contents of a file.|
|ls	| List the contents of the current directory.|
|cd directory-name |	Change into an existing directory.|
|cd ..	| Change backward into an existing directory.|
|cd directory-name/sub-directory-name	| Change forward on multiple directories.|
|cd ../..	| Change backward on multiple directories.|
|clear | Clear the command line screen.|

| Shortcut | Description |
|---|---|
|tab	|Complete the name of an existing file or directory being typed.|
|↑/↓	|Retype commands that were previously written.|
|command + k	|Clear the command line screen.|

## Command Reference Table

| Command | Description |
|---|---|
| mkdir | Create a new directory from the current directory. |
| touch | Create and save a new file. |
| echo "text" > file | Overwrite existing content in file with "text". |
| echo "this text" >> file | Write "this text" to existing content in file. |
| cat file-a > file-b | Overwrite content of file-b with content of file-a. |
| cat file-a >> file-b | Add content of file-a to content of file-b. |
| mv source-file target-file | Move/rename the source-file into the target-file. |
| mv source-directory target-directory | Move/rename the source-directory into the target-directory. |
| rm file | Delete a file. |
| rm -r directory | Delete a non-empty directory. |
| rmdir directory | Delete an empty directory. |
| cp file-a > file-b | Copy content of file-a into a file-b (overwriting anything already inside). |
| cp -r directory-a directory-b | Copy content of directory-a into a directory-b (overwriting anything already inside). |

## Shell Operators Table

| Operator | Description | Example |
|---|---|---|
| > | Overwrite the contents of a file with the results of a command. | echo "Hello, World" > file.txt |
| >> | Add the result of a command to the end of a file. | echo "Hello, World" >> file.txt |
| ; | Run multiple commands in a row, one after another. | echo "Howdy there!" ; cat file.xt |
| \|\| | Logical OR: Runs an alternative command if the first one fails. | mkdir work || echo "Directory creation failed. Does it already exist?" |
| && | Logical AND: Runs the next command if the first one succeeds. | mkdir video-games && cd video-games |
