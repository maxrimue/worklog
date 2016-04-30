# worklog
worklog is a lightweight tool to create, read and modify worklogs inside
your project's path.

# install
```bash
# 1. Get the source code
git clone https://github.com/maxrimue/worklog && cd worklog

# 2. Install the bin
make install

# If installing fails, run with sudo instead
sudo make install
```

# usage
Wherever you are, just type `worklog`, and worklog will open the log
in your current working directory. If there is no `worklog` file, worklog will ask whether to create one in the current working directory.

By default, worklog will use `nano`, but you can also choose what editor to use. All you need to do is to run the following command inside your shell:
```
export EDITOR=<bin>
```
`bin` needs to be an absolute path to a binary, or the name of a globally installed editor. For example:
```
export EDITOR=vim
export EDITOR=vi
export EDITOR=atom
```
**Note that this will only affect your current shell session**. In order to make this permanent, place the code inside a file that gets executed every time you open your shell, examples are:
```bash
# OS X
~/.bash_profile
# Linux
~/.bashrc
```

## ignore
You can also tell `worklog` to automatically make `git` ignore the `worklog` file by running `worklog ignore`, which will insert this into the `.gitignore` of your current working directory:
```bash
#Ignore worklog
worklog
```
If no `.gitignore` is present, a new one will be created.

## today
If you run `worklog today`, worklog will create and open the `worklog` file as usual, but places a new line at the end of the file stating the current date of your operating system. This can be handy if you quickly want to write things down without having to enter the date of the new entry. Example:
```bash
worklog today
```
```bash
==> Sa 30 Apr 2016 20:53:57 CEST
```
