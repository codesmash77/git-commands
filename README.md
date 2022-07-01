# git-commands-
Sample app for learning git commands

##Personal Notes

git init

touch index.html

git config --global user.name ‘Gokul’

git config --global user.email ‘Gokul@gmail.com’

git add index.html

git rm --cached index.html

git add *.html

git status

git add .  \\adding all modified and unmodified files to the staging area.

git commit  \\manual commit by entering i to be in insert mode and then typing initial commit desc, then press esc and then enter :wq to get out of editor gui.

git commit -m ‘changed app.js’ \\committing without using editor gui inside command line.

git branch login

git checkout login \\switching to the login branch from the master branch.

git commit -m ‘login form’

git merge login \\to merge login branch with master branch.

git clean -n \\to see a dry run.

git clean -f -d \\to remove untracked directories.

git remote add origin https://github.com/codesmash77/git-commands-.git

git push -u origin main




###GIT REBASE
If we have the following situation:

    E---F---G---H---I---J  topicA
then the command

git rebase --onto topicA~5 topicA~3 topicA
would result in the removal of commits F and G:

    E---H'---I'---J'  topicA

Where   --onto topicA~5 implies commit E and topicA~3 is the keepbase.

If a conflict is encountered while rebasing, git will indicate which files are conflicting and need to be modified. 
After changes have been made, the changes need to be staged to the commit and then the rebase can resume using git rebase --continue. 
There is also the option of running git rebase --abort while resolving conflicts in a rebase, which will cancel the rebase and leave the branch unchanged.

The golden rule of rebasing is to not rebase public branches.

References : https://medium.com/osedea/git-rebase-powerful-command-507bbac4a234

