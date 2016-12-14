## Equivalent commands
### Commit and push to server
```bash
svn commit -m 'blah'
```
```bash
git commit -m 'blah'
git push
```
A higher authority might be imposing a move to git from Subversion at work. Some
considerations that have crossed my mind.

### Offline working
Doesn't exist in Subversion. Unless you're running your server locally.

git still allows you full config control (bar pushing to github) without a
connection. Which is essential on the train where I do my best work.
