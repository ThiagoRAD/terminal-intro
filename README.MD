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
