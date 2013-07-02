# Git tip of the day

## Checking out a file on a different branch.
It may happen that you are working on a branch, but you need a file that is on a 
different branch. Meet `git checkout branch_name file_pattern`

Assuming you are on master and you need a file called foo-bar.md on
the feauture-foo-bar branch:
    $ git co feature-foo-bar foo-bar.md

This will checkout the specific file in your current working tree.

