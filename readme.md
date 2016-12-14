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
### Offline working
Doesn't exist in Subversion. Unless you're running your server locally.

git still allows you full config control (bar pushing to github) without a
connection. Which is essential on the train where I do my best work.

### Diff with the server
GIT doesn't let you do this quite like Subversion, which is its normal MO. How
do you know if the server copy has changed?

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
