# mono-repo-test-subtree-merge

This mono repo experiment adds iOS and React Native via this method:   
```
cd path/to/project-b
git remote add project-a path/to/project-a
git fetch project-a
git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge
git remote remove project-a
```
http://stackoverflow.com/questions/1425892/how-do-you-merge-two-git-repositories/10548919#10548919
   
And Android via this method:   
```
git remote add -f spoon-knife git@github.com:octocat/Spoon-Knife.git
git merge -s ours --no-commit --allow-unrelated-histories spoon-knife/master
git read-tree --prefix=spoon-knife/ -u spoon-knife/master
git commit -m "Subtree merged in spoon-knife"
```
https://help.github.com/articles/about-git-subtree-merges/

