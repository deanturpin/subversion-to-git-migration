A higher authority might be imposing a move to git from Subversion at work. Some
considerations that have crossed my mind.

## Equivalent commands
### Commit and push to server
```bash
svn commit -m 'blah'
```
```bash
git commit -m 'blah'
git push
```

### Checkout
```bash
svn checkout <repo>
```
```bash
git clone <repo>
```

### Offline working
Doesn't exist in Subversion. Unless you're running your server locally.

git still allows you full config control (bar pushing to github) without a
connection. Which is essential on the train where I do my best work.

### Diff with the server
GIT doesn't let you do this quite like Subversion, which is its normal MO. How
do you know if the server copy has changed?

Neither ```git diff``` nor ```git status``` will tell you if the server has
changed.

```bash
# Create a new branch
git checkout -b prep

# Pull changes from the server master (not the local one)
git pull origin master

# Diff
git diff master

# Checkout our local master
git checkout master

# Merge with the prep branch
git merge prep

# And push it to the server
git push
```

It is quite keen to merge, though. Which I'm not used to. But perhaps we should
be trusting the tools more?

And this does raise the question: should the owner of repo be doing the merge as
part of the review process? I quite like this strategy. 

### Misc
I actually use lots of aliases for common git commands which speeds things up
even more.

```bash
alias gd='git wdiff'
alias gh='git diff HEAD'
alias gl='git log --graph --oneline --decorate --all'

# Commit all and push - equivalent to a Subversion commit
alias gx='git commit -a && git push'
```

See [bash aliases](https://github.com/deanturpin/config).
