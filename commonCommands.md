## Location, FS contents and navigation
- `ls (path)`
   - `ls -a (path)`
- `pwd`
- `cd`
- `.`  Current Directory
- `..` Parent Directory (previous directory)
- `~`  Your home directory (`/home/User/`)

### In practice
- `cd ..` Go back one directory

> You'll often find yourself hitting `ls` as soon as you change into a directory. So this might actually be more like

- `cd ..` , `ls`

- `cd ~` Go to your `home` directory
    - Note that if you run `cd` by itself, it will take to your home directory

## File create, movement and deletion
- `touch` - create a file
- `cp <file> <destination>` - copy a file
  - `cp -R <directory> <destination>` - copy an entire directory (`-R` stands for recursively)
- `mv` - move a file or folder
    - `mv <old file name> <new file name>` - rename a file. seriously!
- `rm <file>` - delete a file
  - `rm -r <file>` - delete an entire directory
##
- `echo` can be used to create new files with text inside of them!
    - normally `echo` is like your terminal's `console.log` - it's used to just log output, like the value of your shell's Environment variables.
      - `echo $USER` (`# would return your username`)
    - however, you can do it with just plain strings as well.
      - `echo 'hello'`
          - *`hello`*
    - we can use a special `>>` operator to pipe output - ANY output, not just that returned from `echo` - into a text file
    - `echo "hello" >> greeting.txt`
        - open the file and you'll `hello` as the first line of text!
    - `echo "hola" >> greeting.txt`
        - because the `>>` operator will *append* to files, we will now have `hola` on the second line.
    - Beware:
      - Don't don't don't use `>` a single chevron / angle bracket operator unless you really mean to do so!
      - `echo "goodbye" > greeting.txt` will overwrite then entire file!
