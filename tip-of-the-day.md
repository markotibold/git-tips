# Git tip of the day

## Checking out a file on a different branch.  It may happen that you are
working on a branch, but you need a file that is on a different branch. Meet
`git checkout branch_name file_pattern`

Assuming you are on master and you need a file called foo-bar.md on the
feauture-foo-bar branch:

    $ git co feature-foo-bar -- foo-bar.md

This will checkout the specific file in your current working tree. The `--` is
optional and implies a path and disambiguates it from a branch with the same
name.


## Making a local shared git repo
Here's how you setup a git repository locally to collaborate with your peers. The setup is as follows:

- one main repo from which you and your peers will pull/fetch/push
- a clone of that repo on which you will be working
- Your peers will need to have file access to the main repo, e.g. through `afp` or `smb`

In the .git/config file inside your main repo:

- set git.config.sharedRepository to 2 
- set git.config.bare to true 

Then:

- create a user for each peer and make put them all in the same group

- recursively add group write permissions to the entire directory of the main repo: 

        $ git chmod -R g+w .  

Start hacking away!

