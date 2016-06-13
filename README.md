Git Model
=====================

Create a feature branch
-----------------------

Create new branch

    git checkout master
    git pull
    git checkout -b myfeature

Once completed committing changes, merge into master

    git checkout master
    git pull
    git merge --no-ff myfeature
    git branch -d myfeature
    git push origin master

OR create a pull request and let another dev review and merge

    git checkout master
    git pull
    git checkout myfeature
    git rebase master

You might have conflicts when rebasing into master. Fix each one and add them:

    git add <filename>
    <repeat for all conflicts>
    git rebase --continue

Once you have rebased successfully you can push the branch to github

    git push origin myfeature

Login into github and you will see the branch that you just pushed. Create a pull request and wait for the code to be revie
