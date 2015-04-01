# bash hats
Reusable command history and better completion for people who wear a lot of
hats. To setup:

```sh
$ . bash-hats
```

## What hats do
```sh
$ cd ~/tmp
$ hat init
$ echo hi > foo         # this command is recorded
```

Then, sometime later on, and from a different shell:

```sh
$ cd ~/tmp
hat: using /home/spencertipping/tmp
$ history 1
echo hi > foo
$ hat ? foo             # tell me about this file or command
echo hi > foo
$ echo <tab>            # history-based tab completion
$ echo hi <tab>
$ echo hi > <tab>
$ echo hi > foo
```

All context is stored in a `.bash-hat` file in the directory from which you ran
`hat init`. Like with git and other systems, hats propagate into
subdirectories.
