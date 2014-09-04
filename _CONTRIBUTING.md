##Git Workflow##
<h3> Starting Up
  - Make your own fork of the repo from Github.com
  - Clone down your fork
  - Create a remote head on logos/master
````
> git remote add production https://github.com/Solano-Ventures/logos.git
````


<h3> Making Contributions
  - Navigate to your 'master' head:
````
> git checkout master
````
  - Pull down the latest state of the production Repo
````
> git pull --rebase production master
````
  - On the Github.com Solano-Ventures project page, make a new issue for the work you want to do

  - Create a new branch for the work you want to do:
    - feat/
    - fix/
    - doc/
    - cleanup/

````
> git checkout -b feat/thing_im_building
````
  - Do your work, making commits as you go
````
> git commit -m 'add part1 of thing'
````
  - When you're done with your feature use rebase to make sure it doesn't conflict with the current state of production
````
> git pull --rebase production master
````
  - If everything looks good, use git rebase -i to squash any commits you dont want
````
> git rebase -i production/master
````
  - Push to your Fork
````
> git push origin feat/thing_im_building
````
  - Go to GitHub.com and make a pull request, use the @username to signal to the team that you've got a pull request
  - As a team, responding to pull requests is really important, so if you see one, take a minute to check it out
  - If the pull request looks good, merge it - the team member responsible for the merge is also responsible for closing out the issue.
  - Done! Let me know if you have any questions: _mccloud.christopher@gmail.com_
