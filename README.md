# bash hats
Reusable command history and better completion for people who wear a lot of
hats. To setup:

```sh
$ . bash-hats
```

Be sure to source bash hats _after_ any other cd-overloading scripts like RVM.

## What hats do
```sh
$ cd ~/tmp
$ hat init
$ echo hi > foo         # this command is recorded
```

Then, sometime later on from a different shell:

```sh
$ cd ~/tmp
hat: using /home/spencertipping/tmp
$ history 1
echo hi > foo
$ echo <tab>            # history-based tab completion
$ echo hi > foo
```

## Commands
```sh
$ hat init              # creates a hat for this directory
$ hat use ~/tmp         # dons the hat for ~/tmp
$ hat dissoc            # undons the current hat
$ hat ls echo           # prints all history containing "echo"
$ hat ls '> foo'        # prints all commands writing to the file foo
$ hat ? foo             # same as 'hat ls "> foo"'
$ hat status            # shows current hat
```

All context is stored in a `.bash-hat` file in the directory from which you ran
`hat init`. Like with git and other systems, hats propagate into
subdirectories.
